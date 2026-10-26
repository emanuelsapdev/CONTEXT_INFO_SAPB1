# SAFTProductTypeEnum — Tipo de producto SAF-T

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `SAFTProductTypeEnum`
- **Descripción (ES):** Tipo de producto SAF-T
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `saftpt_Products` | 0 | Products | Productos |
| `saftpt_Services` | 1 | Services | Servicios |
| `saftpt_Other` | 2 | Other | Otros |
| `saftpt_Taxes` | 3 | Taxes | Impuestos |
| `saftpt_NonSystem` | 4 | Non System | No del sistema |

## Used by (2 properties)

- [AdditionalExpense](../Entidades/AdditionalExpenses.md).`SAFTProductType`
- [Item](../Entidades/Items.md).`SAFTProductType`
