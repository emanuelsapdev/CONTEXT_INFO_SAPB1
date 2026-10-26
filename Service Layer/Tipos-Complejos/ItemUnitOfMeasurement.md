# ItemUnitOfMeasurement — Unidad de medida del artículo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ItemUnitOfMeasurement`
- **Descripción (ES):** Unidad de medida del artículo
- **Description (EN):** Item Unit Of Measurement
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 23

## Properties (23)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `UoMType` | [ItemUoMTypeEnum](../Enums/ItemUoMTypeEnum.md) | Yes | Uo M Type | Tipo de unidad de medida |
| 2 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |
| 3 | `DefaultBarcode` | Edm.Int32 | Yes | Default Barcode | Código de barras predeterminado |
| 4 | `DefaultPackage` | Edm.Int32 | Yes | Default Package | Paquete predeterminado |
| 5 | `Length1` | Edm.Double | Yes | Length 1 | Longitud 1 |
| 6 | `Length1Unit` | Edm.Int32 | Yes | Length 1 Unit | Unidad de longitud 1 |
| 7 | `Length2` | Edm.Double | Yes | Length 2 | Longitud 2 |
| 8 | `Length2Unit` | Edm.Int32 | Yes | Length 2 Unit | Unidad de longitud 2 |
| 9 | `Width1` | Edm.Double | Yes | Width 1 | Ancho 1 |
| 10 | `Width1Unit` | Edm.Int32 | Yes | Width 1 Unit | Unidad de ancho 1 |
| 11 | `Width2` | Edm.Double | Yes | Width 2 | Ancho 2 |
| 12 | `Width2Unit` | Edm.Int32 | Yes | Width 2 Unit | Unidad de ancho 2 |
| 13 | `Height1` | Edm.Double | Yes | Height 1 | Altura 1 |
| 14 | `Height1Unit` | Edm.Int32 | Yes | Height 1 Unit | Unidad de altura 1 |
| 15 | `Height2` | Edm.Double | Yes | Height 2 | Altura 2 |
| 16 | `Height2Unit` | Edm.Int32 | Yes | Height 2 Unit | Unidad de altura 2 |
| 17 | `Volume` | Edm.Double | Yes | Volume | Volumen |
| 18 | `VolumeUnit` | Edm.Int32 | Yes | Volume Unit | Unidad de volumen |
| 19 | `Weight1` | Edm.Double | Yes | Weight 1 | Peso 1 |
| 20 | `Weight1Unit` | Edm.Int32 | Yes | Weight 1 Unit | Unidad de peso 1 |
| 21 | `Weight2` | Edm.Double | Yes | Weight 2 | Peso 2 |
| 22 | `Weight2Unit` | Edm.Int32 | Yes | Weight 2 Unit | Unidad de peso 2 |
| 23 | `ItemUoMPackageCollection` | Collection([ItemUoMPackage](../Tipos-Complejos/ItemUoMPackage.md)) | Yes | Item Uo M Package Collection | Colección de paquetes por unidad de medida del artículo |

## Used by (properties)

- [Item](../Entidades/Items.md).`ItemUnitOfMeasurementCollection`
