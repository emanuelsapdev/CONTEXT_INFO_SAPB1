# ProductTrees — Listas de materiales (árbol de producto)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ProductTrees`
- **Descripción (ES):** Listas de materiales (árbol de producto)
- **Entity type:** `ProductTree` (open type: accepts dynamic/UDF properties)
- **Key:** `TreeCode` (Edm.String)
- **DB tables (main / lines):** [OITT](../../Tablas%20SAP%20B1/OITT.md), [ITT1](../../Tablas%20SAP%20B1/ITT1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 17 · **Navigation properties:** 6 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ProductTrees?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ProductTrees/$count` | Contar |
| Get by key | `GET /b1s/v2/ProductTrees('value')` | Obtener por clave |
| Create | `POST /b1s/v2/ProductTrees` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ProductTrees('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ProductTrees('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/ProductTrees('value')` (only if the B1 object allows removal) | Borrar |

## Properties (17)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TreeCode` 🔑 | Edm.String | No | Tree Code | Código del árbol (lista de materiales) |
| 2 | `TreeType` | [BoItemTreeTypes](../Enums/BoItemTreeTypes.md) | Yes | Tree Type | Tipo de árbol (lista de materiales) |
| 3 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 4 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 5 | `Project` | Edm.String | Yes | Project | Proyecto |
| 6 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 7 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 8 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 9 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |
| 10 | `PriceList` | Edm.Int32 | Yes | Price List | Lista de precios |
| 11 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |
| 12 | `PlanAvgProdSize` | Edm.Double | Yes | Plan Avg Prod Size | Tamaño medio de producción planificado |
| 13 | `HideBOMComponentsInPrintout` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Hide BOM Components In Printout | Ocultar componentes de la lista de materiales en la impresión |
| 14 | `ProductDescription` | Edm.String | Yes | Product Description | Descripción del producto |
| 15 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 16 | `ProductTreeLines` | Collection([ProductTreeLine](../Tipos-Complejos/ProductTreeLine.md)) | Yes | Product Tree Lines | Líneas de la lista de materiales |
| 17 | `ProductTreeStages` | Collection([ProductTreeStage](../Tipos-Complejos/ProductTreeStage.md)) | Yes | Product Tree Stages | Etapas de la lista de materiales |

## Navigation properties (6)

Use `GET /b1s/v2/ProductTrees('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Item` | [Item](../Entidades/Items.md) | [Items](Items.md) | TreeCode → ItemCode | Artículos |
| `DistributionRule6` | [DistributionRule](../Entidades/DistributionRules.md) | [DistributionRules](DistributionRules.md) | DistributionRule → FactorCode | Normas de reparto |
| `Project2` | [Project](../Entidades/Projects.md) | [Projects](Projects.md) | Project → Code | Proyectos |
| `PriceList2` | [PriceList](../Entidades/PriceLists.md) | [PriceLists](PriceLists.md) | PriceList → PriceListNo | Listas de precios |
| `Attachments2` | [Attachments2](../Entidades/Attachments2.md) | [Attachments2](Attachments2.md) | AttachmentEntry → AbsoluteEntry | Anexos |
| `ProductionOrders` | Collection([ProductionOrder](../Entidades/ProductionOrders.md)) | [ProductionOrders](ProductionOrders.md) |  | Órdenes de fabricación |
