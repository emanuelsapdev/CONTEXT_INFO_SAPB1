# WTGroups — Grupos de retención

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WTGroups`
- **Descripción (ES):** Grupos de retención
- **Description (EN):** Withholding Tax Groups
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `WTAbsEntry` | Edm.Int32 | Yes | Withholding Tax Abs Entry | Entrada absoluta de retención |
| 2 | `Percent` | Edm.Double | Yes | Percent | Porcentaje |
| 3 | `SumVATAmount` | Edm.Double | Yes | Sum VAT Amount | Suma del importe de IVA |
| 4 | `SumDocTotal` | Edm.Double | Yes | Sum Document Total | Suma del total de documentos |
| 5 | `SumBaseAmount` | Edm.Double | Yes | Sum Base Amount | Suma del importe base |
| 6 | `SumAccumAmount` | Edm.Double | Yes | Sum Accum Amount | Suma del importe acumulado |
| 7 | `SumPerceptAmount` | Edm.Double | Yes | Sum Percept Amount | Suma del importe de percepción |
| 8 | `DocsInWTGroupsCollection` | Collection([DocsInWTGroups](../Tipos-Complejos/DocsInWTGroups.md)) | Yes | Documents In Withholding Tax Groups Collection | Colección de documentos en grupos de retención |

## Used by (properties)

- [WithholdingTaxCertificatesData](WithholdingTaxCertificatesData.md).`WTGroupsCollection`
