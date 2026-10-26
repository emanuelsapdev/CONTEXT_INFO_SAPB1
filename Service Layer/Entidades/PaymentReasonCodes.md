# PaymentReasonCodes — Códigos de motivo de pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `PaymentReasonCodes`
- **Descripción (ES):** Códigos de motivo de pago
- **Entity type:** `PaymentReasonCode`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OPYR](../../Tablas%20SAP%20B1/OPYR.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 1 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/PaymentReasonCodes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/PaymentReasonCodes/$count` | Contar |
| Get by key | `GET /b1s/v2/PaymentReasonCodes('value')` | Obtener por clave |
| Create | `POST /b1s/v2/PaymentReasonCodes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/PaymentReasonCodes('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/PaymentReasonCodes('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/PaymentReasonCodes('value')` (only if the B1 object allows removal) | Borrar |

## Properties (1)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |

## Navigation properties (1)

Use `GET /b1s/v2/PaymentReasonCodes('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `SpecificWTHAmountsService` | Collection([SpecificWTHAmounts](../Entidades/SpecificWTHAmountsService.md)) | [SpecificWTHAmountsService](SpecificWTHAmountsService.md) |  | Importes de retención específicos |
