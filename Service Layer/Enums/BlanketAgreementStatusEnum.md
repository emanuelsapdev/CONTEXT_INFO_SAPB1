# BlanketAgreementStatusEnum — Estado del acuerdo global

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BlanketAgreementStatusEnum`
- **Descripción (ES):** Estado del acuerdo global
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `asApproved` | 0 | Approved | Aprobado |
| `asOnHold` | 1 | On Hold | En espera |
| `asDraft` | 2 | Draft | Borrador |
| `asTerminated` | 3 | Terminated | Terminado |
| `asCancelled` | 4 | Cancelled | Cancelado |

## Used by (1 properties)

- [BlanketAgreement](../Entidades/BlanketAgreements.md).`Status`
