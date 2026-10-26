# DocumentAuthorizationStatusEnum — Estado de autorización del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `DocumentAuthorizationStatusEnum`
- **Descripción (ES):** Estado de autorización del documento
- **Underlying type:** Edm.Int32
- **Members:** 7

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `dasWithout` | 0 | Without | Sin autorización |
| `dasPending` | 1 | Pending | Pendiente |
| `dasApproved` | 2 | Approved | Autorizado |
| `dasRejected` | 3 | Rejected | Rechazado |
| `dasGenerated` | 4 | Generated | Generado |
| `dasGeneratedbyAuthorizer` | 5 | Generatedby Authorizer | Generado por el autorizador |
| `dasCancelled` | 6 | Cancelled | Cancelado |

## Used by (1 properties)

- [Document](../Entidades/PurchaseQuotations.md).`AuthorizationStatus`
