# 3.9 Batch Operations (`$batch`)

> Source: *Working with SAP Business One Service Layer* v1.29, section 3.9 (paraphrased technical reference).
>
> **Resumen (ES):** enviar varias operaciones en un solo request HTTP (multipart/mixed), agruparlas en *change sets* atómicos (todo o nada), referenciar entidades recién creadas con `Content-ID` y leer la respuesta.

## Overview

| Aspect | Detail | Detalle (ES) |
|---|---|---|
| Format | Multipart MIME v1.0 message | Mensaje MIME multiparte |
| Method / URI | Always `POST <service root>/$batch`, e.g. `POST https://dbserver:50000/b1s/v1/$batch` | Siempre POST a `$batch` |
| Header | `Content-Type: multipart/mixed;boundary=<Batch Boundary>` | Cabecera con el boundary |
| Execution | Parts are processed **sequentially**, in order | Se ejecutan en orden |
| Change set | Atomic unit: if one sub-request fails, the whole change set is **rolled back** | Unidad atómica (rollback total) |
| Change set restrictions | No `GET` and no nested change sets inside a change set | Sin GET ni change sets anidados |
| Response code | `202 Accepted` (OData v3) or `200 OK` (OData v4) when the format is valid; `400` if the batch format is invalid | Código de respuesta |

## Body structure

```
--<Batch Boundary>
<sub-request 1>
--<Batch Boundary>
<sub-request 2>
--<Batch Boundary>
Content-Type: multipart/mixed;boundary=<Changeset Boundary>

--<Changeset Boundary>
<change set sub-request 1>
--<Changeset Boundary>
<change set sub-request 2>
--<Changeset Boundary>--
--<Batch Boundary>--
```

Each sub-request part needs these headers, then a blank line, then the HTTP request (request line, headers, blank line, body):

```
Content-Type: application/http
Content-Transfer-Encoding: binary
```

For a `GET` sub-request you need **two empty lines** after the request line: the first ends the GET headers, the second is its empty body (followed by CRLF).

## Content-ID references (change sets only)

- Inside a change set, an entity created by a `POST` can be referenced later in the same change set as **`$<Content-ID>`** (an alias of the new entity URI).
- OData v3: `Content-ID` only needed when you reference it. **OData v4: `Content-ID` is mandatory** on every change set part.

```
--changeset
Content-Type: application/http
Content-Transfer-Encoding: binary
Content-ID: 1

POST /b1s/v1/Items
<item JSON>
--changeset
Content-Type: application/http
Content-Transfer-Encoding: binary
Content-ID: 2

PATCH /b1s/v1/$1
<item update JSON>
--changeset--
```

## Complete sample (query + change set with insert and update)

```http
POST https://dbserver:50000/b1s/v1/$batch
OData-Version: 4.0
Content-Type: multipart/mixed;boundary=batch_36522ad7-fc75-4b56-8c71-56071383e77b

--batch_36522ad7-fc75-4b56-8c71-56071383e77b
Content-Type: application/http
Content-Transfer-Encoding: binary

GET /b1s/v1/Items('i001')


--batch_36522ad7-fc75-4b56-8c71-56071383e77b
Content-Type: multipart/mixed;boundary=changeset_77162fcd-b8da-41ac-a9f8-9357efbbd

--changeset_77162fcd-b8da-41ac-a9f8-9357efbbd
Content-Type: application/http
Content-Transfer-Encoding: binary
Content-ID: 1

POST /b1s/v1/Items('i002')
Content-Type: application/json

<item i002 JSON>
--changeset_77162fcd-b8da-41ac-a9f8-9357efbbd
Content-Type: application/http
Content-Transfer-Encoding: binary
Content-ID: 2

PATCH /b1s/v1/$1
Content-Type: application/json

<item i002 update JSON>
--changeset_77162fcd-b8da-41ac-a9f8-9357efbbd--
--batch_36522ad7-fc75-4b56-8c71-56071383e77b--
```

## Responses

| Situation | What you get | Situación (ES) |
|---|---|---|
| Invalid batch format | `400 Bad Request`, e.g. `{"error": {"code": -1000, "message": {"value": "Incomplete Batch Request Body!"}}}` | Formato inválido |
| All OK | One sub-response per sub-request inside `--batchresponse_...` parts; change set responses inside `--changesetresponse_...` with their `Content-ID` (e.g. `201 Created` + `Location`, then `204 No Content`) | Todo correcto |
| A sub-request fails | Execution **stops at the failing part**. A failed change set returns **a single response** for the whole change set (e.g. `400` "Item code 'i002' already exists"), regardless of how many parts it had | Error: se detiene y el change set devuelve una sola respuesta |

Example of a success response fragment:

```
--batchresponse_d878...
Content-Type: application/http
Content-Transfer-Encoding: binary

HTTP/1.1 200 OK
Content-Type: application/json;odata=minimalmetadata;charset=utf-8
<Item i001 JSON>
--batchresponse_d878...
Content-Type: multipart/mixed;boundary=changesetresponse_8bfb...

--changesetresponse_8bfb...
Content-ID: 1
HTTP/1.1 201 Created
Location: https://dbserver:50000/b1s/v1/Items('i002')
<Item i002 JSON>
--changesetresponse_8bfb...
Content-ID: 2
HTTP/1.1 204 No Content
--changesetresponse_8bfb...--
--batchresponse_d878...--
```

## Example: create an order and cancel it in one transaction

```
POST https://dbserver:50000/b1s/v1/$batch
Content-Type: multipart/mixed;boundary=batch_1

--batch_1
Content-Type: multipart/mixed;boundary=changeset_1

--changeset_1
Content-Type: application/http
Content-Transfer-Encoding: binary
Content-ID: 1

POST Orders
Host: host

{ "CardCode": "c1", "DocDueDate": "2017-07-20",
  "DocumentLines": [ { "ItemCode": "i1", "Quantity": "1", "TaxCode": "t1", "UnitPrice": "30" } ] }
--changeset_1
Content-Type: application/http
Content-Transfer-Encoding: binary

POST $1/Cancel
Host: host

--changeset_1--
--batch_1--
```

For multi-step business logic that can't be expressed as a change set (e.g. using the response of one step to build the next), use the **JavaScript extensions** with `startTransaction/commitTransaction` (see [03-10](03-10-JavaScript-Extensions.md)).
