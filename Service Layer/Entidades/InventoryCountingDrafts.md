# InventoryCountingDrafts — Borradores de recuento de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `InventoryCountingDrafts`
- **Descripción (ES):** Borradores de recuento de inventario
- **Entity type:** `InventoryCountingDraft` (open type: accepts dynamic/UDF properties)
- **Key:** `DocumentEntry` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 17 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/InventoryCountingDrafts?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/InventoryCountingDrafts/$count` | Contar |
| Get by key | `GET /b1s/v2/InventoryCountingDrafts(1)` | Obtener por clave |
| Create | `POST /b1s/v2/InventoryCountingDrafts` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/InventoryCountingDrafts(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/InventoryCountingDrafts(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/InventoryCountingDrafts(1)` (only if the B1 object allows removal) | Borrar |

## Properties (17)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocumentEntry` 🔑 | Edm.Int32 | No | Document Entry | Entrada del documento |
| 2 | `DocumentNumber` | Edm.Int32 | Yes | Document Number | Número de documento |
| 3 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 4 | `CountDate` | Edm.DateTimeOffset | Yes | Count Date | Fecha de recuento |
| 5 | `CountTime` | Edm.TimeOfDay | Yes | Count Time | Hora de recuento |
| 6 | `SingleCounterType` | [CounterTypeEnum](../Enums/CounterTypeEnum.md) | Yes | Single Counter Type | Tipo de contador único |
| 7 | `SingleCounterID` | Edm.Int32 | Yes | Single Counter ID | ID de contador único |
| 8 | `DocumentStatus` | [CountingDocumentStatusEnum](../Enums/CountingDocumentStatusEnum.md) | Yes | Document Status | Estado del documento |
| 9 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 10 | `Reference2` | Edm.String | Yes | Reference 2 | Referencia 2 |
| 11 | `BranchID` | Edm.Int32 | Yes | Branch ID | ID de sucursal |
| 12 | `DocObjectCodeEx` | Edm.String | Yes | Document Object Code Ex | Código de objeto del documento (ampliado) |
| 13 | `FinancialPeriod` | Edm.Int32 | Yes | Financial Period | Período contable |
| 14 | `PeriodIndicator` | Edm.String | Yes | Period Indicator | Indicador de período |
| 15 | `CountingType` | [CountingTypeEnum](../Enums/CountingTypeEnum.md) | Yes | Counting Type | Tipo de recuento |
| 16 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 17 | `YearEndDate` | Edm.DateTimeOffset | Yes | Year End Date | Fecha de fin de año |

## Navigation properties (2)

Use `GET /b1s/v2/InventoryCountingDrafts(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPlace` | [BusinessPlace](../Entidades/BusinessPlaces.md) | [BusinessPlaces](BusinessPlaces.md) | BranchID → BPLID | Lugar de negocios |
| `Attachments2` | [Attachments2](../Entidades/Attachments2.md) | [Attachments2](Attachments2.md) | AttachmentEntry → AbsoluteEntry | Anexos |
