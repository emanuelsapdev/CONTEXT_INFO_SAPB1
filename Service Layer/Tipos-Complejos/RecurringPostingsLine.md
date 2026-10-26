# RecurringPostingsLine — Línea de contabilización periódica

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `RecurringPostingsLine`
- **Descripción (ES):** Línea de contabilización periódica
- **Description (EN):** Recurring Postings Line

- **Properties:** 22

## Properties (22)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `RcrCode` | Edm.String | Yes | Rcr Code | Código de recurrencia |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `ControlAccount` | Edm.String | Yes | Control Account | Cuenta asociada |
| 4 | `AccountCode` | Edm.String | Yes | Account Code | Código de cuenta |
| 5 | `AccountName` | Edm.String | Yes | Account Name | Nombre de cuenta |
| 6 | `Debit` | Edm.Double | Yes | Debit | Debe/Débito |
| 7 | `Credit` | Edm.Double | Yes | Credit | Haber/Crédito |
| 8 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 9 | `TaxGroup` | Edm.String | Yes | Tax Group | Grupo de impuestos |
| 10 | `VatLine` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Vat Line | Línea de IVA |
| 11 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 12 | `TaxPostingAccount` | [BoTaxPostingAccountTypeEnum](../Enums/BoTaxPostingAccountTypeEnum.md) | Yes | Tax Posting Account | Cuenta de contabilización de impuestos |
| 13 | `TaxCode` | Edm.String | Yes | Tax Code | Indicador de impuesto |
| 14 | `CostingCode1` | Edm.String | Yes | Costing Code 1 | Norma de reparto 1 |
| 15 | `CostingCode2` | Edm.String | Yes | Costing Code 2 | Norma de reparto (dimensión 2) |
| 16 | `CostingCode3` | Edm.String | Yes | Costing Code 3 | Norma de reparto (dimensión 3) |
| 17 | `CostingCode4` | Edm.String | Yes | Costing Code 4 | Norma de reparto (dimensión 4) |
| 18 | `CostingCode5` | Edm.String | Yes | Costing Code 5 | Norma de reparto (dimensión 5) |
| 19 | `WTaxLiable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | W Tax Liable | Sujeto a retención |
| 20 | `WTaxLine` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | W Tax Line | Línea de retención |
| 21 | `ProjectCode` | Edm.String | Yes | Project Code | Código de proyecto |
| 22 | `CostElementCode` | Edm.String | Yes | Cost Element Code | Código de elemento de costo |

## Used by (properties)

- [RecurringPostings](../Entidades/RecurringPostings.md).`RecurringPostingsLineCollection`
