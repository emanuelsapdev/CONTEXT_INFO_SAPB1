# StockTransferAuthorizationStatusEnum — Estado de autorización de la transferencia de stock

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `StockTransferAuthorizationStatusEnum`
- **Descripción (ES):** Estado de autorización de la transferencia de stock
- **Underlying type:** Edm.Int32
- **Members:** 7

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `sasWithout` | 0 | Without | Sin autorización |
| `sasPending` | 1 | Pending | Pendiente |
| `sasApproved` | 2 | Approved | Autorizado |
| `sasRejected` | 3 | Rejected | Rechazado |
| `sasGenerated` | 4 | Generated | Generado |
| `sasGeneratedbyAuthorizer` | 5 | Generatedby Authorizer | Generado por el autorizador |
| `sasCancelled` | 6 | Cancelled | Cancelado |

## Used by (1 properties)

- [StockTransfer](../Entidades/StockTransfers.md).`AuthorizationStatus`
