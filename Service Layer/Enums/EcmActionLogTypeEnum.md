# EcmActionLogTypeEnum — Tipo de registro de acción ECM

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `EcmActionLogTypeEnum`
- **Descripción (ES):** Tipo de registro de acción ECM
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `altSend` | 1 | Send | Envío |
| `altReceive` | 2 | Receive | Recepción |
| `altImport` | 3 | Import | Importación |
| `altNote` | 4 | Note | Nota |
| `altWarning` | 5 | Warning | Advertencia |
| `altError` | 6 | Error | Error |

## Used by (1 properties)

- [EcmActionLog](../Tipos-Complejos/EcmActionLog.md).`Type`
