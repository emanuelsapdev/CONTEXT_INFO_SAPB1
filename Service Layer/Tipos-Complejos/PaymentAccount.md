# PaymentAccount — Cuentas del pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PaymentAccount`
- **Descripción (ES):** Cuentas del pago
- **Description (EN):** Payment Account
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 17

## Properties (17)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `AccountCode` | Edm.String | Yes | Account Code | Código de cuenta |
| 3 | `SumPaid` | Edm.Double | Yes | Sum Paid | Importe pagado |
| 4 | `SumPaidFC` | Edm.Double | Yes | Sum Paid FC (foreign currency) | Importe pagado (ME) |
| 5 | `Decription` | Edm.String | Yes | Decription | Descripción |
| 6 | `VatGroup` | Edm.String | Yes | Vat Group | Grupo de IVA (indicador de impuesto) |
| 7 | `AccountName` | Edm.String | Yes | Account Name | Nombre de cuenta |
| 8 | `GrossAmount` | Edm.Double | Yes | Gross Amount | Importe bruto |
| 9 | `ProfitCenter` | Edm.String | Yes | Profit Center | Centro de beneficio |
| 10 | `ProjectCode` | Edm.String | Yes | Project Code | Código de proyecto |
| 11 | `VatAmount` | Edm.Double | Yes | Vat Amount | Importe de IVA |
| 12 | `ProfitCenter2` | Edm.String | Yes | Profit Center 2 | Centro de beneficio 2 |
| 13 | `ProfitCenter3` | Edm.String | Yes | Profit Center 3 | Centro de beneficio 3 |
| 14 | `ProfitCenter4` | Edm.String | Yes | Profit Center 4 | Centro de beneficio 4 |
| 15 | `ProfitCenter5` | Edm.String | Yes | Profit Center 5 | Centro de beneficio 5 |
| 16 | `LocationCode` | Edm.Int32 | Yes | Location Code | Código de ubicación |
| 17 | `EqualizationVatAmount` | Edm.Double | Yes | Equalization Vat Amount | Importe de IVA de recargo de equivalencia |

## Used by (properties)

- [Payment](../Entidades/VendorPayments.md).`PaymentAccounts`
