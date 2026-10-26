# UnitOfMeasurements — Unidades de medida

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `UnitOfMeasurements`
- **Descripción (ES):** Unidades de medida
- **Entity type:** `UnitOfMeasurement` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OUOM](../../Tablas%20SAP%20B1/OUOM.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 27 · **Navigation properties:** 6 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/UnitOfMeasurements?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/UnitOfMeasurements/$count` | Contar |
| Get by key | `GET /b1s/v2/UnitOfMeasurements(1)` | Obtener por clave |
| Create | `POST /b1s/v2/UnitOfMeasurements` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/UnitOfMeasurements(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/UnitOfMeasurements(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/UnitOfMeasurements(1)` (only if the B1 object allows removal) | Borrar |

## Properties (27)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Name` | Edm.String | Yes | Name | Nombre |
| 4 | `Length1` | Edm.Double | Yes | Length 1 | Longitud 1 |
| 5 | `Length1Unit` | Edm.Int32 | Yes | Length 1 Unit | Unidad de longitud 1 |
| 6 | `Length2` | Edm.Double | Yes | Length 2 | Longitud 2 |
| 7 | `Length2Unit` | Edm.Int32 | Yes | Length 2 Unit | Unidad de longitud 2 |
| 8 | `Width1` | Edm.Double | Yes | Width 1 | Ancho 1 |
| 9 | `Width1Unit` | Edm.Int32 | Yes | Width 1 Unit | Unidad de ancho 1 |
| 10 | `Width2` | Edm.Double | Yes | Width 2 | Ancho 2 |
| 11 | `Width2Unit` | Edm.Int32 | Yes | Width 2 Unit | Unidad de ancho 2 |
| 12 | `Height1` | Edm.Double | Yes | Height 1 | Altura 1 |
| 13 | `Height1Unit` | Edm.Int32 | Yes | Height 1 Unit | Unidad de altura 1 |
| 14 | `Height2` | Edm.Double | Yes | Height 2 | Altura 2 |
| 15 | `Height2Unit` | Edm.Int32 | Yes | Height 2 Unit | Unidad de altura 2 |
| 16 | `Volume` | Edm.Double | Yes | Volume | Volumen |
| 17 | `VolumeUnit` | Edm.Int32 | Yes | Volume Unit | Unidad de volumen |
| 18 | `Weight1` | Edm.Double | Yes | Weight 1 | Peso 1 |
| 19 | `Weight1Unit` | Edm.Int32 | Yes | Weight 1 Unit | Unidad de peso 1 |
| 20 | `Weight2` | Edm.Double | Yes | Weight 2 | Peso 2 |
| 21 | `Weight2Unit` | Edm.Int32 | Yes | Weight 2 Unit | Unidad de peso 2 |
| 22 | `InternationalSymbol` | Edm.String | Yes | International Symbol | Símbolo internacional |
| 23 | `EWBUnitEntry` | Edm.Int32 | Yes | EWB Unit Entry | Unidad EWB |
| 24 | `PPWeight1` | Edm.Double | Yes | PP Weight 1 | Peso 1 del envase plástico |
| 25 | `PPWe1Unit` | Edm.Int32 | Yes | PP We 1 Unit | Unidad de peso 1 del envase plástico |
| 26 | `PPWeight2` | Edm.Double | Yes | PP Weight 2 | Peso 2 del envase plástico |
| 27 | `PPWe2Unit` | Edm.Int32 | Yes | PP We 2 Unit | Unidad de peso 2 del envase plástico |

## Navigation properties (6)

Use `GET /b1s/v2/UnitOfMeasurements(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ItemGroups` | Collection([ItemGroups](../Entidades/ItemGroups.md)) | [ItemGroups](ItemGroups.md) |  | Grupos de artículos |
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `BinLocations` | Collection([BinLocation](../Entidades/BinLocations.md)) | [BinLocations](BinLocations.md) |  | Ubicaciones (bin locations) |
| `BarCodes` | Collection([BarCode](../Entidades/BarCodes.md)) | [BarCodes](BarCodes.md) |  | Códigos de barras |
| `UnitOfMeasurementGroups` | Collection([UnitOfMeasurementGroup](../Entidades/UnitOfMeasurementGroups.md)) | [UnitOfMeasurementGroups](UnitOfMeasurementGroups.md) |  | Grupos de unidades de medida |
| `ProductionOrders` | Collection([ProductionOrder](../Entidades/ProductionOrders.md)) | [ProductionOrders](ProductionOrders.md) |  | Órdenes de fabricación |
