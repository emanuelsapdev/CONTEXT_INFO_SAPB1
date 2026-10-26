# BoEquipmentBPType — Tipo de socio de negocios del equipo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoEquipmentBPType`
- **Descripción (ES):** Tipo de socio de negocios del equipo
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `et_Sales` | 1 | Sales | Ventas |
| `et_Purchasing` | 2 | Purchasing | Compras |
| `et_SalesAndPurchasing` | 3 | Sales And Purchasing | Ventas y compras |

## Used by (1 properties)

- [CustomerEquipmentCard](../Entidades/CustomerEquipmentCards.md).`ServiceBPType`
