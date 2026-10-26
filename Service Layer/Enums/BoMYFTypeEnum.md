# BoMYFTypeEnum — Tipo MYF (Grecia)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoMYFTypeEnum`
- **Descripción (ES):** Tipo MYF (Grecia)
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `myft_WholesaleSales` | 0 | Wholesale Sales | Ventas mayoristas |
| `myft_RetailSales` | 1 | Retail Sales | Ventas minoristas |
| `myft_WholesalePurchases` | 2 | Wholesale Purchases | Compras mayoristas |
| `myft_OtherExpenseTransactions` | 3 | Other Expense Transactions | Otras transacciones de gastos |

## Used by (1 properties)

- [BPAddress](../Tipos-Complejos/BPAddress.md).`MYFType`
