# NFTaxCategories — Categorías de impuestos de Nota Fiscal

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `NFTaxCategories`
- **Descripción (ES):** Categorías de impuestos de Nota Fiscal
- **Entity type:** `NFTaxCategory`
- **Key:** `AbsId` (Edm.Int32)
- **DB tables (main / lines):** [ONFT](../../Tablas%20SAP%20B1/ONFT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/NFTaxCategories?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/NFTaxCategories/$count` | Contar |
| Get by key | `GET /b1s/v2/NFTaxCategories(1)` | Obtener por clave |
| Create | `POST /b1s/v2/NFTaxCategories` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/NFTaxCategories(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/NFTaxCategories(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/NFTaxCategories(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsId` 🔑 | Edm.Int32 | No | Abs ID | ID absoluto |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Locked` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Locked | Bloqueado |
| 4 | `GPCId` | Edm.Int32 | Yes | GPC ID | ID GPC |
| 5 | `CESTrel` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | CES Trel | Relevante para CEST |

## Navigation properties (2)

Use `GET /b1s/v2/NFTaxCategories(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `GovPayCode` | [GovPayCode](../Entidades/GovPayCodes.md) | [GovPayCodes](GovPayCodes.md) | GPCId → AbsId | Códigos de pago gubernamental |
| `NotaFiscalCST` | Collection([NotaFiscalCST](../Entidades/NotaFiscalCST.md)) | [NotaFiscalCST](NotaFiscalCST.md) |  | CST de Nota Fiscal |
