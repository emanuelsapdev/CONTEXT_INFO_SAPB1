# NotaFiscalCST — CST de Nota Fiscal

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `NotaFiscalCST`
- **Descripción (ES):** CST de Nota Fiscal
- **Entity type:** `NotaFiscalCST` (open type: accepts dynamic/UDF properties)
- **Key:** `ID` (Edm.Int32)
- **DB tables (main / lines):** [OTSC](../../Tablas%20SAP%20B1/OTSC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/NotaFiscalCST?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/NotaFiscalCST/$count` | Contar |
| Get by key | `GET /b1s/v2/NotaFiscalCST(1)` | Obtener por clave |
| Create | `POST /b1s/v2/NotaFiscalCST` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/NotaFiscalCST(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/NotaFiscalCST(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/NotaFiscalCST(1)` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ID` 🔑 | Edm.Int32 | No | ID | ID |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Situation` | Edm.String | Yes | Situation | Situación |
| 4 | `TaxCategory` | Edm.Int32 | Yes | Tax Category | Categoría de impuesto |
| 5 | `CSTCodeOutgoing` | Edm.String | Yes | CST Code Outgoing | Código CST de salida |
| 6 | `DescriptionOutgoing` | Edm.String | Yes | Description Outgoing | Descripción de salida |

## Navigation properties (2)

Use `GET /b1s/v2/NotaFiscalCST(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `WithholdingTaxCodes` | Collection([WithholdingTaxCode](../Entidades/WithholdingTaxCodes.md)) | [WithholdingTaxCodes](WithholdingTaxCodes.md) |  | Códigos de retención de impuestos |
| `NFTaxCategory` | [NFTaxCategory](../Entidades/NFTaxCategories.md) | [NFTaxCategories](NFTaxCategories.md) | TaxCategory → AbsId | Categorías de impuestos de Nota Fiscal |
