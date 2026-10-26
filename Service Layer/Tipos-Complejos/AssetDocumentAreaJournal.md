# AssetDocumentAreaJournal — Asiento por área del documento de activo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AssetDocumentAreaJournal`
- **Descripción (ES):** Asiento por área del documento de activo
- **Description (EN):** Asset Document Area Journal

- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `DepreciationArea` | Edm.String | Yes | Depreciation Area | Área de amortización |
| 4 | `JournalRemarks` | Edm.String | Yes | Journal Remarks | Comentarios del asiento |
| 5 | `TransactionNumber` | Edm.Int32 | Yes | Transaction Number | Número de transacción |
| 6 | `CancellationJournalRemarks` | Edm.String | Yes | Cancellation Journal Remarks | Comentarios del asiento de cancelación |
| 7 | `CancellationTransactionNumber` | Edm.Int32 | Yes | Cancellation Transaction Number | Número de transacción de cancelación |

## Used by (properties)

- [AssetDocument](../Entidades/AssetRetirement.md).`AssetDocumentAreaJournalCollection`
