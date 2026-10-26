# InventoryOpeningBalances — Saldos iniciales de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `InventoryOpeningBalances`
- **Descripción (ES):** Saldos iniciales de inventario
- **Entity type:** `InventoryOpeningBalance` (open type: accepts dynamic/UDF properties)
- **Key:** `DocumentEntry` (Edm.Int32)
- **DB tables (main / lines):** [OIQI](../../Tablas%20SAP%20B1/OIQI.md), [IQI1](../../Tablas%20SAP%20B1/IQI1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 16 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/InventoryOpeningBalances?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/InventoryOpeningBalances/$count` | Contar |
| Get by key | `GET /b1s/v2/InventoryOpeningBalances(1)` | Obtener por clave |
| Create | `POST /b1s/v2/InventoryOpeningBalances` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/InventoryOpeningBalances(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/InventoryOpeningBalances(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/InventoryOpeningBalances(1)` (only if the B1 object allows removal) | Borrar |

## Properties (16)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocumentEntry` 🔑 | Edm.Int32 | No | Document Entry | Entrada del documento |
| 2 | `PostingDate` | Edm.DateTimeOffset | Yes | Posting Date | Fecha de contabilización |
| 3 | `DocumentDate` | Edm.DateTimeOffset | Yes | Document Date | Fecha del documento |
| 4 | `DocumentNumber` | Edm.Int32 | Yes | Document Number | Número de documento |
| 5 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 6 | `Reference2` | Edm.String | Yes | Reference 2 | Referencia 2 |
| 7 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 8 | `BranchID` | Edm.Int32 | Yes | Branch ID | ID de sucursal |
| 9 | `PriceSource` | [InventoryOpeningBalancePriceSourceEnum](../Enums/InventoryOpeningBalancePriceSourceEnum.md) | Yes | Price Source | Origen del precio |
| 10 | `PriceList` | Edm.Int32 | Yes | Price List | Lista de precios |
| 11 | `JournalRemark` | Edm.String | Yes | Journal Remark | Comentario del asiento |
| 12 | `DocObjectCodeEx` | Edm.String | Yes | Document Object Code Ex | Código de objeto del documento (ampliado) |
| 13 | `PeriodIndicator` | Edm.String | Yes | Period Indicator | Indicador de período |
| 14 | `FinancialPeriod` | Edm.Int32 | Yes | Financial Period | Período contable |
| 15 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 16 | `InventoryOpeningBalanceLines` | Collection([InventoryOpeningBalanceLine](../Tipos-Complejos/InventoryOpeningBalanceLine.md)) | Yes | Inventory Opening Balance Lines | Líneas del saldo inicial de inventario |

## Navigation properties (2)

Use `GET /b1s/v2/InventoryOpeningBalances(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPlace` | [BusinessPlace](../Entidades/BusinessPlaces.md) | [BusinessPlaces](BusinessPlaces.md) | BranchID → BPLID | Lugar de negocios |
| `Attachments2` | [Attachments2](../Entidades/Attachments2.md) | [Attachments2](Attachments2.md) | AttachmentEntry → AbsoluteEntry | Anexos |
