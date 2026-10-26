# AssetOriginalTypeEnum — Tipo original del activo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `AssetOriginalTypeEnum`
- **Descripción (ES):** Tipo original del activo
- **Underlying type:** Edm.Int32
- **Members:** 11

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `aotARInvoice` | 0 | AR Invoice | Factura de clientes |
| `aotAPCreditMemo` | 1 | AP Credit Memo | Nota de crédito de proveedores |
| `aotAPInvoice` | 2 | AP Invoice | Factura de proveedores |
| `aotOutgoingPayment` | 3 | Outgoing Payment | Pago efectuado |
| `aotAPCorrectionInvoice` | 4 | AP Correction Invoice | Factura de corrección de proveedores |
| `aotCapitalization` | 5 | Capitalization | Capitalización |
| `aotFixedAssetsCreditMemo` | 6 | Fixed Assets Credit Memo | Nota de crédito de activos fijos |
| `aotAllTransactions` | 7 | All Transactions | Todas las transacciones |
| `aotManualDepreciation` | 8 | Manual Depreciation | Amortización manual |
| `aotFixedAssetsTransfer` | 9 | Fixed Assets Transfer | Transferencia de activos fijos |
| `aotRetirement` | 10 | Retirement | Baja |

## Used by (1 properties)

- [AssetDocument](../Entidades/AssetRetirement.md).`OriginalType`
