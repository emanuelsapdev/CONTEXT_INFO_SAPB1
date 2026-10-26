# EBooks — Libros electrónicos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `EBooks`
- **Descripción (ES):** Libros electrónicos
- **Entity type:** `EBooks`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OEBK](../../Tablas%20SAP%20B1/OEBK.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 19 · **Navigation properties:** 0 · **Bound actions:** 2

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/EBooks?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/EBooks/$count` | Contar |
| Get by key | `GET /b1s/v2/EBooks(1)` | Obtener por clave |
| Create | `POST /b1s/v2/EBooks` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/EBooks(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/EBooks(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/EBooks(1)` (only if the B1 object allows removal) | Borrar |
| Action `GetByMark` | `POST /b1s/v2/EBooks(1)/GetByMark` | Obtener por MARK |
| Action `GetByDocKey` | `POST /b1s/v2/EBooks(1)/GetByDocKey` | Obtener por clave de documento |

## Properties (19)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `MARK` | Edm.String | Yes | MARK | MARK (Grecia) |
| 3 | `CancelMARK` | Edm.String | Yes | Cancel MARK | Marca de cancelación |
| 4 | `UID` | Edm.String | Yes | UID | UID |
| 5 | `IssuerVATID` | Edm.String | Yes | Issuer VATID | ID de IVA del emisor |
| 6 | `CPVATID` | Edm.String | Yes | CPVATID | ID de IVA de la persona de contacto |
| 7 | `Series` | Edm.String | Yes | Series | Serie de numeración |
| 8 | `AA` | Edm.String | Yes | AA | Código AA |
| 9 | `IssueDate` | Edm.DateTimeOffset | Yes | Issue Date | Fecha de emisión |
| 10 | `InvoiceType` | Edm.String | Yes | Invoice Type | Tipo de factura |
| 11 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 12 | `TotalNetValue` | Edm.Double | Yes | Total Net Value | Valor neto total |
| 13 | `TotalVatAmount` | Edm.Double | Yes | Total Vat Amount | Importe total de IVA |
| 14 | `TotalWithheldAmount` | Edm.Double | Yes | Total Withheld Amount | Importe total retenido |
| 15 | `TotalGrossValue` | Edm.Double | Yes | Total Gross Value | Valor bruto total |
| 16 | `LinkedDocType` | Edm.Int32 | Yes | Linked Document Type | Tipo de documento vinculado |
| 17 | `LinkedDocEntry` | Edm.Int32 | Yes | Linked Document Entry | DocEntry del documento vinculado |
| 18 | `IsNegativeMark` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Negative Mark | Es marca negativa |
| 19 | `EBooksLines` | Collection([EBooksLine](../Tipos-Complejos/EBooksLine.md)) | Yes | E Books Lines | Líneas de libros electrónicos |

## Bound actions (2)

### GetByMark

- **Descripción (ES):** Obtener por MARK
- **Request:** `POST /b1s/v2/EBooks(1)/GetByMark`
- **Returns:** [EBooks](../Entidades/EBooks.md)

### GetByDocKey

- **Descripción (ES):** Obtener por clave de documento
- **Request:** `POST /b1s/v2/EBooks(1)/GetByDocKey`
- **Returns:** Collection([EBooksParams](../Tipos-Complejos/EBooksParams.md))

