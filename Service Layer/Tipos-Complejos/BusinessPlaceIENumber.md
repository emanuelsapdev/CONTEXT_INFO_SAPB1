# BusinessPlaceIENumber — Números de I.E. del lugar de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BusinessPlaceIENumber`
- **Descripción (ES):** Números de I.E. del lugar de negocios
- **Description (EN):** Business Place IE Number
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |
| 2 | `State` | Edm.String | Yes | State | Estado/provincia |
| 3 | `IENumber` | Edm.String | Yes | IE Number | Número de I.E. (inscripción estatal) |

## Used by (properties)

- [BusinessPlace](../Entidades/BusinessPlaces.md).`BusinessPlaceIENumbers`
