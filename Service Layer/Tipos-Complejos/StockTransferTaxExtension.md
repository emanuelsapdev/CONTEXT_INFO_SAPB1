# StockTransferTaxExtension — Extensión de impuestos de la transferencia de stock

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `StockTransferTaxExtension`
- **Descripción (ES):** Extensión de impuestos de la transferencia de stock
- **Description (EN):** Stock Transfer Tax Extension
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `SupportVAT` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Support VAT | Soporta IVA |
| 2 | `FormNumber` | Edm.String | Yes | Form Number | Número de formulario |
| 3 | `TransactionCategory` | Edm.String | Yes | Transaction Category | Categoría de transacción |
| 4 | `U_B1SYS_TrailerId` | Edm.String | Yes | [AR localization] Trailer ID | [Loc. AR] Patente del acoplado/remolque |
| 5 | `U_B1SYS_IncotermsTxt` | Edm.String | Yes | [AR localization] Incoterms Txt | [Loc. AR] Texto de Incoterms |

## Used by (properties)

- [StockTransfer](../Entidades/StockTransfers.md).`StockTransferTaxExtension`
