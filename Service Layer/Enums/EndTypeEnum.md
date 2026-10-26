# EndTypeEnum — Tipo de fin de recurrencia

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `EndTypeEnum`
- **Descripción (ES):** Tipo de fin de recurrencia
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `etNoEndDate` | 0 | Number End Date | Sin fecha de fin |
| `etByCounter` | 1 | By Counter | Por cantidad de ocurrencias |
| `etByDate` | 2 | By Date | Por fecha |

## Used by (2 properties)

- [Activity](../Entidades/Activities.md).`EndType`
- [InventoryCycles](../Entidades/InventoryCycles.md).`endType`
