# DocsInWTGroups — Documentos en grupos de retención

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocsInWTGroups`
- **Descripción (ES):** Documentos en grupos de retención
- **Description (EN):** Documents In Withholding Tax Groups
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `DocObjType` | Edm.String | Yes | Document Obj Type | Tipo de objeto del documento |
| 3 | `VATAmount` | Edm.Double | Yes | VAT Amount | Importe de IVA |
| 4 | `DocTotal` | Edm.Double | Yes | Document Total | Total del documento |
| 5 | `BaseAmount` | Edm.Double | Yes | Base Amount | Importe base |
| 6 | `AccumAmount` | Edm.Double | Yes | Accum Amount | Importe acumulado |
| 7 | `PerceptAmount` | Edm.Double | Yes | Percept Amount | Importe de percepción |
| 8 | `Percent` | Edm.Double | Yes | Percent | Porcentaje |

## Used by (properties)

- [WTGroups](WTGroups.md).`DocsInWTGroupsCollection`
