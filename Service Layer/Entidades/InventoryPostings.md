# InventoryPostings — Contabilizaciones de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `InventoryPostings`
- **Descripción (ES):** Contabilizaciones de inventario
- **Entity type:** `InventoryPosting` (open type: accepts dynamic/UDF properties)
- **Key:** `DocumentEntry` (Edm.Int32)
- **DB tables (main / lines):** [OIQR](../../Tablas%20SAP%20B1/OIQR.md), [IQR1](../../Tablas%20SAP%20B1/IQR1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 19 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/InventoryPostings?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/InventoryPostings/$count` | Contar |
| Get by key | `GET /b1s/v2/InventoryPostings(1)` | Obtener por clave |
| Create | `POST /b1s/v2/InventoryPostings` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/InventoryPostings(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/InventoryPostings(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/InventoryPostings(1)` (only if the B1 object allows removal) | Borrar |

## Properties (19)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocumentEntry` 🔑 | Edm.Int32 | No | Document Entry | Entrada del documento |
| 2 | `DocumentNumber` | Edm.Int32 | Yes | Document Number | Número de documento |
| 3 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 4 | `PostingDate` | Edm.DateTimeOffset | Yes | Posting Date | Fecha de contabilización |
| 5 | `CountDate` | Edm.DateTimeOffset | Yes | Count Date | Fecha de recuento |
| 6 | `CountTime` | Edm.TimeOfDay | Yes | Count Time | Hora de recuento |
| 7 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 8 | `Reference2` | Edm.String | Yes | Reference 2 | Referencia 2 |
| 9 | `BranchID` | Edm.Int32 | Yes | Branch ID | ID de sucursal |
| 10 | `PriceSource` | [InventoryPostingPriceSourceEnum](../Enums/InventoryPostingPriceSourceEnum.md) | Yes | Price Source | Origen del precio |
| 11 | `PriceList` | Edm.Int32 | Yes | Price List | Lista de precios |
| 12 | `JournalRemark` | Edm.String | Yes | Journal Remark | Comentario del asiento |
| 13 | `DocObjectCodeEx` | Edm.String | Yes | Document Object Code Ex | Código de objeto del documento (ampliado) |
| 14 | `FinancialPeriod` | Edm.Int32 | Yes | Financial Period | Período contable |
| 15 | `PeriodIndicator` | Edm.String | Yes | Period Indicator | Indicador de período |
| 16 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 17 | `YearEndDate` | Edm.DateTimeOffset | Yes | Year End Date | Fecha de fin de año |
| 18 | `InventoryPostingLines` | Collection([InventoryPostingLine](../Tipos-Complejos/InventoryPostingLine.md)) | Yes | Inventory Posting Lines | Líneas de la contabilización de inventario |
| 19 | `InventoryPostingDocumentReferencesCollection` | Collection([InventoryPostingDocumentReferences](../Tipos-Complejos/InventoryPostingDocumentReferences.md)) | Yes | Inventory Posting Document References Collection | Referencias de documentos de la contabilización de inventario |

## Navigation properties (2)

Use `GET /b1s/v2/InventoryPostings(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPlace` | [BusinessPlace](../Entidades/BusinessPlaces.md) | [BusinessPlaces](BusinessPlaces.md) | BranchID → BPLID | Lugar de negocios |
| `Attachments2` | [Attachments2](../Entidades/Attachments2.md) | [Attachments2](Attachments2.md) | AttachmentEntry → AbsoluteEntry | Anexos |
