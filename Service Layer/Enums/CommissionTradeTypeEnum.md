# CommissionTradeTypeEnum — Tipo de comercio con comisión

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `CommissionTradeTypeEnum`
- **Descripción (ES):** Tipo de comercio con comisión
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ct_Empty` | 0 | Empty | Vacío |
| `ct_SalesAgent` | 1 | Sales Agent | Agente de ventas |
| `ct_PurchaseAgent` | 2 | Purchase Agent | Agente de compras |
| `ct_Consignor` | 3 | Consignor | Consignador |

## Used by (1 properties)

- [Document](../Entidades/PurchaseQuotations.md).`CommissionTrade`
