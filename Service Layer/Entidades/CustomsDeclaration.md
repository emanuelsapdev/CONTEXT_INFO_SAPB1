# CustomsDeclaration — Declaración aduanera

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `CustomsDeclaration`
- **Descripción (ES):** Declaración aduanera
- **Entity type:** `CustomsDeclaration` (open type: accepts dynamic/UDF properties)
- **Key:** `CCDNum` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 9 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/CustomsDeclaration?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/CustomsDeclaration/$count` | Contar |
| Get by key | `GET /b1s/v2/CustomsDeclaration('value')` | Obtener por clave |
| Create | `POST /b1s/v2/CustomsDeclaration` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/CustomsDeclaration('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/CustomsDeclaration('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/CustomsDeclaration('value')` (only if the B1 object allows removal) | Borrar |

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CCDNum` 🔑 | Edm.String | No | CCD Number | Número de declaración aduanera de carga |
| 2 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 3 | `CustomsBroker` | Edm.String | Yes | Customs Broker | Despachante de aduana |
| 4 | `DocNum` | Edm.String | Yes | Document Number | Número de documento |
| 5 | `DocDate` | Edm.DateTimeOffset | Yes | Document Date | Fecha de contabilización del documento |
| 6 | `SupplyNum` | Edm.String | Yes | Supply Number | Número de suministro |
| 7 | `SupplyDate` | Edm.DateTimeOffset | Yes | Supply Date | Fecha de suministro |
| 8 | `CustomsTerminal` | Edm.String | Yes | Customs Terminal | Terminal aduanera |
| 9 | `PaymentKey` | Edm.String | Yes | Payment Key | Clave de pago |
