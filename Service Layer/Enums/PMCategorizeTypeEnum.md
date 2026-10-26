# PMCategorizeTypeEnum — Tipo de categorización de gestión de proyectos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `PMCategorizeTypeEnum`
- **Descripción (ES):** Tipo de categorización de gestión de proyectos
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `pm_cat_Ignore` | 0 | Cat Ignore | Ignorar |
| `pm_cat_OpenAmountAP` | 1 | Cat Open Amount AP | Importe abierto de compras |
| `pm_cat_OpenAmountAR` | 2 | Cat Open Amount AR | Importe abierto de ventas |
| `pm_cat_InvoicedAP` | 3 | Cat Invoiced AP | Facturado de compras |
| `pm_cat_InvoicedAR` | 4 | Cat Invoiced AR | Facturado de ventas |

## Used by (2 properties)

- [PMS_DocumentData](../Tipos-Complejos/PMS_DocumentData.md).`Categorize`
- [PM_DocumentData](../Tipos-Complejos/PM_DocumentData.md).`Categorize`
