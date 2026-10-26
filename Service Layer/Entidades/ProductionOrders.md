# ProductionOrders — Órdenes de fabricación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ProductionOrders`
- **Descripción (ES):** Órdenes de fabricación
- **Entity type:** `ProductionOrder` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsoluteEntry` (Edm.Int32)
- **DB tables (main / lines):** [OWOR](../../Tablas%20SAP%20B1/OWOR.md), [WOR1](../../Tablas%20SAP%20B1/WOR1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 44 · **Navigation properties:** 9 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ProductionOrders?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ProductionOrders/$count` | Contar |
| Get by key | `GET /b1s/v2/ProductionOrders(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ProductionOrders` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ProductionOrders(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ProductionOrders(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ProductionOrders(1)` (only if the B1 object allows removal) | Borrar |
| Action `Cancel` | `POST /b1s/v2/ProductionOrders(1)/Cancel` | Cancelar |

## Properties (44)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsoluteEntry` 🔑 | Edm.Int32 | No | Absolute Entry | Entrada absoluta (ID interno) |
| 2 | `DocumentNumber` | Edm.Int32 | Yes | Document Number | Número de documento |
| 3 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 4 | `ItemNo` | Edm.String | Yes | Item Number | Número de artículo |
| 5 | `ProductionOrderStatus` | [BoProductionOrderStatusEnum](../Enums/BoProductionOrderStatusEnum.md) | Yes | Production Order Status | Estado de la orden de fabricación |
| 6 | `ProductionOrderType` | [BoProductionOrderTypeEnum](../Enums/BoProductionOrderTypeEnum.md) | Yes | Production Order Type | Tipo de orden de fabricación |
| 7 | `PlannedQuantity` | Edm.Double | Yes | Planned Quantity | Cantidad planificada |
| 8 | `CompletedQuantity` | Edm.Double | Yes | Completed Quantity | Cantidad completada |
| 9 | `RejectedQuantity` | Edm.Double | Yes | Rejected Quantity | Cantidad rechazada |
| 10 | `PostingDate` | Edm.DateTimeOffset | Yes | Posting Date | Fecha de contabilización |
| 11 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 12 | `ProductionOrderOriginEntry` | Edm.Int32 | Yes | Production Order Origin Entry | Entrada de origen de la orden de fabricación |
| 13 | `ProductionOrderOriginNumber` | Edm.Int32 | Yes | Production Order Origin Number | Número de origen de la orden de fabricación |
| 14 | `ProductionOrderOrigin` | [BoProductionOrderOriginEnum](../Enums/BoProductionOrderOriginEnum.md) | Yes | Production Order Origin | Origen de la orden de fabricación |
| 15 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 16 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 17 | `ClosingDate` | Edm.DateTimeOffset | Yes | Closing Date | Fecha de cierre |
| 18 | `ReleaseDate` | Edm.DateTimeOffset | Yes | Release Date | Fecha de liberación |
| 19 | `CustomerCode` | Edm.String | Yes | Customer Code | Código de cliente |
| 20 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |
| 21 | `InventoryUOM` | Edm.String | Yes | Inventory Unit of Measure | Unidad de medida de inventario |
| 22 | `JournalRemarks` | Edm.String | Yes | Journal Remarks | Comentarios del asiento |
| 23 | `TransactionNumber` | Edm.Int32 | Yes | Transaction Number | Número de transacción |
| 24 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 25 | `Printed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Printed | Impreso |
| 26 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 27 | `Project` | Edm.String | Yes | Project | Proyecto |
| 28 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 29 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 30 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 31 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |
| 32 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |
| 33 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 34 | `ProductDescription` | Edm.String | Yes | Product Description | Descripción del producto |
| 35 | `Priority` | Edm.Int32 | Yes | Priority | Prioridad |
| 36 | `RoutingDateCalculation` | [ResourceAllocationEnum](../Enums/ResourceAllocationEnum.md) | Yes | Routing Date Calculation | Cálculo de fecha de ruta |
| 37 | `UpdateAllocation` | [BoUpdateAllocationEnum](../Enums/BoUpdateAllocationEnum.md) | Yes | Update Allocation | Actualizar asignación |
| 38 | `SAPPassport` | Edm.String | Yes | SAP Passport | SAP Passport |
| 39 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 40 | `PickRemarks` | Edm.String | Yes | Pick Remarks | Comentarios de picking |
| 41 | `ProductionOrderLines` | Collection([ProductionOrderLine](../Tipos-Complejos/ProductionOrderLine.md)) | Yes | Production Order Lines | Líneas de la orden de fabricación |
| 42 | `ProductionOrdersSalesOrderLines` | Collection([ProductionOrdersSalesOrderLine](../Tipos-Complejos/ProductionOrdersSalesOrderLine.md)) | Yes | Production Orders Sales Order Lines | Líneas de pedido de cliente de la orden de fabricación |
| 43 | `ProductionOrdersStages` | Collection([ProductionOrdersStage](../Tipos-Complejos/ProductionOrdersStage.md)) | Yes | Production Orders Stages | Etapas de la orden de fabricación |
| 44 | `ProductionOrdersDocumentReferences` | Collection([ProductionOrdersDocumentReference](../Tipos-Complejos/ProductionOrdersDocumentReference.md)) | Yes | Production Orders Document References | Referencias de documentos de la orden de fabricación |

## Navigation properties (9)

Use `GET /b1s/v2/ProductionOrders(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ProductTree` | [ProductTree](../Entidades/ProductTrees.md) | [ProductTrees](ProductTrees.md) | ItemNo → TreeCode | Listas de materiales (árbol de producto) |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | UserSignature → InternalKey | Usuario |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CustomerCode → CardCode | Socio de negocios |
| `Warehouse2` | [Warehouse](../Entidades/Warehouses.md) | [Warehouses](Warehouses.md) | Warehouse → WarehouseCode | Almacenes |
| `JournalEntry` | [JournalEntry](../Entidades/JournalEntries.md) | [JournalEntries](JournalEntries.md) | TransactionNumber → JdtNum | Asientos contables |
| `DistributionRule6` | [DistributionRule](../Entidades/DistributionRules.md) | [DistributionRules](DistributionRules.md) | DistributionRule → FactorCode | Normas de reparto |
| `Project2` | [Project](../Entidades/Projects.md) | [Projects](Projects.md) | Project → Code | Proyectos |
| `UnitOfMeasurement` | [UnitOfMeasurement](../Entidades/UnitOfMeasurements.md) | [UnitOfMeasurements](UnitOfMeasurements.md) | UoMEntry → AbsEntry | Unidades de medida |
| `Attachments2` | [Attachments2](../Entidades/Attachments2.md) | [Attachments2](Attachments2.md) | AttachmentEntry → AbsoluteEntry | Anexos |

## Bound actions (1)

### Cancel

- **Descripción (ES):** Cancelar
- **Request:** `POST /b1s/v2/ProductionOrders(1)/Cancel`

