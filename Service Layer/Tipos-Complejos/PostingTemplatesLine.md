# PostingTemplatesLine — Línea de plantilla de contabilización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PostingTemplatesLine`
- **Descripción (ES):** Línea de plantilla de contabilización
- **Description (EN):** Posting Templates Line

- **Properties:** 21

## Properties (21)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TrtCode` | Edm.String | Yes | Trt Code | Código TRT |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `ControlAccount` | Edm.String | Yes | Control Account | Cuenta asociada |
| 4 | `AccountCode` | Edm.String | Yes | Account Code | Código de cuenta |
| 5 | `AccountName` | Edm.String | Yes | Account Name | Nombre de cuenta |
| 6 | `Debit` | Edm.Double | Yes | Debit | Debe/Débito |
| 7 | `Credit` | Edm.Double | Yes | Credit | Haber/Crédito |
| 8 | `TaxGroup` | Edm.String | Yes | Tax Group | Grupo de impuestos |
| 9 | `VatLine` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Vat Line | Línea de IVA |
| 10 | `TaxPostingAccount` | [BoTaxPostingAccountTypeEnum](../Enums/BoTaxPostingAccountTypeEnum.md) | Yes | Tax Posting Account | Cuenta de contabilización de impuestos |
| 11 | `TaxCode` | Edm.String | Yes | Tax Code | Indicador de impuesto |
| 12 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 13 | `CostingCode1` | Edm.String | Yes | Costing Code 1 | Norma de reparto 1 |
| 14 | `CostingCode2` | Edm.String | Yes | Costing Code 2 | Norma de reparto (dimensión 2) |
| 15 | `CostingCode3` | Edm.String | Yes | Costing Code 3 | Norma de reparto (dimensión 3) |
| 16 | `CostingCode4` | Edm.String | Yes | Costing Code 4 | Norma de reparto (dimensión 4) |
| 17 | `CostingCode5` | Edm.String | Yes | Costing Code 5 | Norma de reparto (dimensión 5) |
| 18 | `WTaxLiable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | W Tax Liable | Sujeto a retención |
| 19 | `WTaxLine` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | W Tax Line | Línea de retención |
| 20 | `ProjectCode` | Edm.String | Yes | Project Code | Código de proyecto |
| 21 | `CostElementCode` | Edm.String | Yes | Cost Element Code | Código de elemento de costo |

## Used by (properties)

- [PostingTemplates](../Entidades/PostingTemplates.md).`PostingTemplatesLineCollection`
