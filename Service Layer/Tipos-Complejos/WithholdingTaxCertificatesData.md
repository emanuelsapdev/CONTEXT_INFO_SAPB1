# WithholdingTaxCertificatesData — Datos de certificados de retención

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WithholdingTaxCertificatesData`
- **Descripción (ES):** Datos de certificados de retención
- **Description (EN):** Withholding Tax Certificates Data
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 15

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `POICodeRef` | Edm.String | Yes | POI Code Ref | Referencia del código de punto de emisión |
| 2 | `POICode` | Edm.String | Yes | POI Code | Código de punto de emisión |
| 3 | `Certificate` | Edm.String | Yes | Certificate | Certificado |
| 4 | `WTaxType` | Edm.String | Yes | W Tax Type | Tipo de retención |
| 5 | `PeriodIndicator` | Edm.String | Yes | Period Indicator | Indicador de período |
| 6 | `WhtAbsId` | Edm.Int32 | Yes | Wht Abs ID | ID absoluto de retención |
| 7 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 8 | `Number` | Edm.Int32 | Yes | Number | Número |
| 9 | `IssueDate` | Edm.DateTimeOffset | Yes | Issue Date | Fecha de emisión |
| 10 | `SumVATAmount` | Edm.Double | Yes | Sum VAT Amount | Suma del importe de IVA |
| 11 | `SumDocTotal` | Edm.Double | Yes | Sum Document Total | Suma del total de documentos |
| 12 | `SumBaseAmount` | Edm.Double | Yes | Sum Base Amount | Suma del importe base |
| 13 | `SumAccumAmount` | Edm.Double | Yes | Sum Accum Amount | Suma del importe acumulado |
| 14 | `SumPercAmount` | Edm.Double | Yes | Sum Perc Amount | Suma del importe de percepción |
| 15 | `WTGroupsCollection` | Collection([WTGroups](../Tipos-Complejos/WTGroups.md)) | Yes | Withholding Tax Groups Collection | Colección de grupos de retención |

## Used by (properties)

- [Payment](../Entidades/VendorPayments.md).`WithholdingTaxCertificatesCollection`
