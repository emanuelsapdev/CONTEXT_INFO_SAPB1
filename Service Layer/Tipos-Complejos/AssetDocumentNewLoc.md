# AssetDocumentNewLoc — Nueva ubicación del documento de activo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AssetDocumentNewLoc`
- **Descripción (ES):** Nueva ubicación del documento de activo
- **Description (EN):** Asset Document New Loc

- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `AssetNumber` | Edm.String | Yes | Asset Number | Número de activo |
| 4 | `CurLocation` | Edm.Int32 | Yes | Currency Location | Ubicación actual |
| 5 | `NewLocation` | Edm.Int32 | Yes | New Location | Nueva ubicación |
| 6 | `NBV` | Edm.Double | Yes | NBV | Valor neto contable |
| 7 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |

## Used by (properties)

- [AssetDocument](../Entidades/AssetRetirement.md).`AssetDocumentNewLocCollection`
