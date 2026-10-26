# EDocStatusEnum — Estado del documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `EDocStatusEnum`
- **Descripción (ES):** Estado del documento electrónico
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `edoc_New` | 0 | New | Nuevo |
| `edoc_Pending` | 1 | Pending | Pendiente |
| `edoc_Sent` | 2 | Sent | Enviado |
| `edoc_Error` | 3 | Error | Error |
| `edoc_Ok` | 4 | Ok | Correcto |

## Used by (1 properties)

- [Document](../Entidades/PurchaseQuotations.md).`EDocStatus`
