# ItemUoMPackage — Paquete por unidad de medida del artículo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ItemUoMPackage`
- **Descripción (ES):** Paquete por unidad de medida del artículo
- **Description (EN):** Item Uo M Package
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 22

## Properties (22)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `UoMType` | [ItemUoMTypeEnum](../Enums/ItemUoMTypeEnum.md) | Yes | Uo M Type | Tipo de unidad de medida |
| 2 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |
| 3 | `PackageTypeEntry` | Edm.Int32 | Yes | Package Type Entry | Tipo de paquete |
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
| 22 | `QuantityPerPackage` | Edm.Double | Yes | Quantity Per Package | Cantidad por paquete |

## Used by (properties)

- [ItemUnitOfMeasurement](ItemUnitOfMeasurement.md).`ItemUoMPackageCollection`
