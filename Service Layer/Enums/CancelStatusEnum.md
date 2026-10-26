# CancelStatusEnum — Estado de cancelación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `CancelStatusEnum`
- **Descripción (ES):** Estado de cancelación
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `csYes` | 0 | Yes | Cancelado |
| `csNo` | 1 | Number | No cancelado |
| `csCancellation` | 2 | Cancellation | Documento de cancelación |

## Used by (2 properties)

- [Document](../Entidades/PurchaseQuotations.md).`CancelStatus`
- [Payment](../Entidades/VendorPayments.md).`CancelStatus`
