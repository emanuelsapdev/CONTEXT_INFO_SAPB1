# BinLocations — Ubicaciones (bin locations)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BinLocations`
- **Descripción (ES):** Ubicaciones (bin locations)
- **Entity type:** `BinLocation` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OBIN](../../Tablas%20SAP%20B1/OBIN.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 40 · **Navigation properties:** 7 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BinLocations?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BinLocations/$count` | Contar |
| Get by key | `GET /b1s/v2/BinLocations(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BinLocations` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BinLocations(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BinLocations(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BinLocations(1)` (only if the B1 object allows removal) | Borrar |

## Properties (40)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |
| 3 | `Sublevel1` | Edm.String | Yes | Sublevel 1 | Subnivel 1 |
| 4 | `Sublevel2` | Edm.String | Yes | Sublevel 2 | Subnivel 2 |
| 5 | `Sublevel3` | Edm.String | Yes | Sublevel 3 | Subnivel 3 |
| 6 | `Sublevel4` | Edm.String | Yes | Sublevel 4 | Subnivel 4 |
| 7 | `BinCode` | Edm.String | Yes | Bin Code | Código de ubicación |
| 8 | `Inactive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inactive | Inactivo |
| 9 | `Description` | Edm.String | Yes | Description | Descripción |
| 10 | `AlternativeSortCode` | Edm.String | Yes | Alternative Sort Code | Código de clasificación alternativo |
| 11 | `BarCode` | Edm.String | Yes | Bar Code | Código de barras |
| 12 | `Attribute1` | Edm.String | Yes | Attribute 1 | Atributo 1 |
| 13 | `Attribute2` | Edm.String | Yes | Attribute 2 | Atributo 2 |
| 14 | `Attribute3` | Edm.String | Yes | Attribute 3 | Atributo 3 |
| 15 | `Attribute4` | Edm.String | Yes | Attribute 4 | Atributo 4 |
| 16 | `Attribute5` | Edm.String | Yes | Attribute 5 | Atributo 5 |
| 17 | `Attribute6` | Edm.String | Yes | Attribute 6 | Atributo 6 |
| 18 | `Attribute7` | Edm.String | Yes | Attribute 7 | Atributo 7 |
| 19 | `Attribute8` | Edm.String | Yes | Attribute 8 | Atributo 8 |
| 20 | `Attribute9` | Edm.String | Yes | Attribute 9 | Atributo 9 |
| 21 | `Attribute10` | Edm.String | Yes | Attribute 10 | Atributo 10 |
| 22 | `RestrictedItemType` | [BinRestrictItemEnum](../Enums/BinRestrictItemEnum.md) | Yes | Restricted Item Type | Tipo de artículo restringido |
| 23 | `SpecificItem` | Edm.String | Yes | Specific Item | Artículo específico |
| 24 | `SpecificItemGroup` | Edm.Int32 | Yes | Specific Item Group | Grupo de artículos específico |
| 25 | `BatchRestrictions` | [BinRestrictionBatchEnum](../Enums/BinRestrictionBatchEnum.md) | Yes | Batch Restrictions | Restricciones de lote |
| 26 | `RestrictedTransType` | [BinRestrictTransactionEnum](../Enums/BinRestrictTransactionEnum.md) | Yes | Restricted Trans Type | Tipo de transacción restringido |
| 27 | `RestrictionReason` | Edm.String | Yes | Restriction Reason | Motivo de restricción |
| 28 | `DateRestrictionChanged` | Edm.DateTimeOffset | Yes | Date Restriction Changed | Restricción de fecha modificada |
| 29 | `MinimumQty` | Edm.Double | Yes | Minimum Quantity | Cantidad mínima |
| 30 | `MaximumQty` | Edm.Double | Yes | Maximum Quantity | Cantidad máxima |
| 31 | `IsSystemBin` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is System Bin | Es ubicación del sistema |
| 32 | `ReceivingBinLocation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Receiving Bin Location | Ubicación de recepción |
| 33 | `ExcludeAutoAllocOnIssue` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Exclude Auto Alloc On Issue | Excluir asignación automática en salida |
| 34 | `MaximumWeight` | Edm.Double | Yes | Maximum Weight | Peso máximo |
| 35 | `MaximumWeight1` | Edm.Double | Yes | Maximum Weight 1 | Peso máximo 1 |
| 36 | `MaximumWeightUnit` | Edm.Int32 | Yes | Maximum Weight Unit | Unidad de peso máximo |
| 37 | `MaximumWeightUnit1` | Edm.Int32 | Yes | Maximum Weight Unit 1 | Unidad de peso máximo 1 |
| 38 | `RestrictedUoMType` | [BinRestrictUoMEnum](../Enums/BinRestrictUoMEnum.md) | Yes | Restricted Uo M Type | Tipo de unidad de medida restringido |
| 39 | `SpecificUoM` | Edm.Int32 | Yes | Specific Uo M | Unidad de medida específica |
| 40 | `SpecificUoMGroup` | Edm.Int32 | Yes | Specific Uo M Group | Grupo de unidades de medida específico |

## Navigation properties (7)

Use `GET /b1s/v2/BinLocations(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Warehouses` | Collection([Warehouse](../Entidades/Warehouses.md)) | [Warehouses](Warehouses.md) |  | Almacenes |
| `Warehouse2` | [Warehouse](../Entidades/Warehouses.md) | [Warehouses](Warehouses.md) | Warehouse → WarehouseCode | Almacenes |
| `Item` | [Item](../Entidades/Items.md) | [Items](Items.md) | SpecificItem → ItemCode | Artículos |
| `ItemGroups` | [ItemGroups](../Entidades/ItemGroups.md) | [ItemGroups](ItemGroups.md) | SpecificItemGroup → Number | Grupos de artículos |
| `WeightMeasure` | [WeightMeasure](../Entidades/WeightMeasures.md) | [WeightMeasures](WeightMeasures.md) | MaximumWeightUnit → UnitCode | Unidades de peso |
| `UnitOfMeasurement` | [UnitOfMeasurement](../Entidades/UnitOfMeasurements.md) | [UnitOfMeasurements](UnitOfMeasurements.md) | SpecificUoM → AbsEntry | Unidades de medida |
| `UnitOfMeasurementGroup` | [UnitOfMeasurementGroup](../Entidades/UnitOfMeasurementGroups.md) | [UnitOfMeasurementGroups](UnitOfMeasurementGroups.md) | SpecificUoMGroup → AbsEntry | Grupos de unidades de medida |
