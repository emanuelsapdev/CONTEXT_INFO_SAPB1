# ElecCommStatusEnum — Estado de comunicación electrónica

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ElecCommStatusEnum`
- **Descripción (ES):** Estado de comunicación electrónica
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ecsApproved` | 0 | Approved | Aprobado |
| `ecsPendingApproval` | 1 | Pending Approval | Pendiente de aprobación |
| `ecsRejected` | 2 | Rejected | Rechazado |

## Used by (3 properties)

- [Document](../Entidades/PurchaseQuotations.md).`ElecCommStatus`
- [Payment](../Entidades/VendorPayments.md).`ElecCommStatus`
- [StockTransfer](../Entidades/StockTransfers.md).`ElecCommStatus`
