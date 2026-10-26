# FolioLetterEnum — Letra del comprobante (Argentina)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `FolioLetterEnum`
- **Descripción (ES):** Letra del comprobante (Argentina)
- **Underlying type:** Edm.Int32
- **Members:** 9

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `fLetterA` | 0 | Letter A | Letra A |
| `fLetterB` | 1 | Letter B | Letra B |
| `fLetterC` | 2 | Letter C | Letra C |
| `fLetterE` | 3 | Letter E | Letra E |
| `fLetterM` | 4 | Letter M | Letra M |
| `fLetterR` | 5 | Letter R | Letra R |
| `fLetterT` | 5 | Letter T | Letra T |
| `fLetterX` | 5 | Letter X | Letra X |
| `fLetterEMPTY` | 5 | Letter EMPTY | Sin letra |

## Used by (3 properties)

- [Document](../Entidades/PurchaseQuotations.md).`Letter`
- [JournalEntry](../Entidades/JournalEntries.md).`Letter`
- [StockTransfer](../Entidades/StockTransfers.md).`Letter`
