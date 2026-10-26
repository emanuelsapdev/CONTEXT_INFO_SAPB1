# BoStatus — Estado del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoStatus`
- **Descripción (ES):** Estado del documento
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bost_Open` | 0 | Open | Abierto |
| `bost_Close` | 1 | Close | Cerrado |
| `bost_Paid` | 2 | Paid | Pagado |
| `bost_Delivered` | 3 | Delivered | Entregado |

## Used by (9 properties)

- [BlanketAgreementsDocument](../Tipos-Complejos/BlanketAgreementsDocument.md).`RowStatus`
- [Document](../Entidades/PurchaseQuotations.md).`DocumentStatus`
- [Document](../Entidades/PurchaseQuotations.md).`InventoryStatus`
- [DocumentAdditionalExpense](../Tipos-Complejos/DocumentAdditionalExpense.md).`Status`
- [DocumentLine](../Tipos-Complejos/DocumentLine.md).`LineStatus`
- [StockTransfer](../Entidades/StockTransfers.md).`DocumentStatus`
- [StockTransferLine](../Tipos-Complejos/StockTransferLine.md).`LineStatus`
- [WithholdingTaxData](../Tipos-Complejos/WithholdingTaxData.md).`Status`
- [WithholdingTaxLine](../Tipos-Complejos/WithholdingTaxLine.md).`Status`
