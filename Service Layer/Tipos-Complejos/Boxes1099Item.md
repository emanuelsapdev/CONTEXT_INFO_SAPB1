# Boxes1099Item — Casilla 1099

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `Boxes1099Item`
- **Descripción (ES):** Casilla 1099
- **Description (EN):** Boxes 1099 Item
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FormCode` | Edm.Int32 | Yes | Form Code | Código de formulario |
| 2 | `Box1099` | Edm.String | Yes | Box 1099 | Casilla 1099 |
| 3 | `BoxDescription` | Edm.String | Yes | Box Description | Descripción de la casilla |
| 4 | `Minimum1099Amount` | Edm.Double | Yes | Minimum 1099 Amount | Importe mínimo 1099 |

## Used by (properties)

- [Forms1099](../Entidades/Forms1099.md).`Boxes1099`
