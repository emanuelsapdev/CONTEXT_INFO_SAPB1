# DocumentPackageItem — Artículos de paquetes del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocumentPackageItem`
- **Descripción (ES):** Artículos de paquetes del documento
- **Description (EN):** Document Package Item
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PackageNumber` | Edm.Int32 | Yes | Package Number | Número de paquete |
| 2 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 3 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 4 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |
| 5 | `MeasureUnit` | Edm.String | Yes | Measure Unit | Unidad de medida |
| 6 | `UnitsOfMeasurement` | Edm.Double | Yes | Units Of Measurement | Unidades de medida |

## Used by (properties)

- [DocumentPackage](DocumentPackage.md).`DocumentPackageItems`
