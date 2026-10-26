# BoBpAccountTypes — Tipo de cuenta asociada del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoBpAccountTypes`
- **Descripción (ES):** Tipo de cuenta asociada del socio de negocios
- **Underlying type:** Edm.Int32
- **Members:** 15

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bpat_General` | 0 | General | General |
| `bpat_DownPayment` | 1 | Down Payment | Anticipos |
| `bpat_AssetsAccount` | 2 | Assets Account | Cuenta de activos |
| `bpat_Receivable` | 3 | Receivable | Por cobrar |
| `bpat_Payable` | 4 | Payable | Por pagar |
| `bpat_OnCollection` | 5 | On Collection | En cobranza |
| `bpat_Presentation` | 6 | Presentation | Presentación |
| `bpat_AssetsPayable` | 7 | Assets Payable | Activos por pagar |
| `bpat_Discounted` | 8 | Discounted | Descontado |
| `bpat_Unpaid` | 9 | Unpaid | Impago |
| `bpat_OpenDebts` | 10 | Open Debts | Deudas abiertas |
| `bpat_Domestic` | 11 | Domestic | Nacional |
| `bpat_Foreign` | 12 | Foreign | Exterior |
| `bpat_CashDiscountInterim` | 13 | Cash Discount Interim | Transitoria de descuento por pronto pago |
| `bpat_ExchangeRateInterim` | 14 | Exchange Rate Interim | Transitoria de tipo de cambio |

## Used by (1 properties)

- [BPAccountReceivablePayble](../Tipos-Complejos/BPAccountReceivablePayble.md).`AccountType`
