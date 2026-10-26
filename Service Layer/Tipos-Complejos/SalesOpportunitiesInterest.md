# SalesOpportunitiesInterest — Intereses de la oportunidad de venta

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SalesOpportunitiesInterest`
- **Descripción (ES):** Intereses de la oportunidad de venta
- **Description (EN):** Sales Opportunities Interest
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `RowNo` | Edm.Int32 | Yes | Row Number | Número de línea |
| 2 | `SequenceNo` | Edm.Int32 | Yes | Sequence Number | Número de secuencia |
| 3 | `PrimaryInterest` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Primary Interest | Interés principal |
| 4 | `InterestId` | Edm.Int32 | Yes | Interest ID | ID de interés |

## Used by (properties)

- [SalesOpportunities](../Entidades/SalesOpportunities.md).`SalesOpportunitiesInterests`
