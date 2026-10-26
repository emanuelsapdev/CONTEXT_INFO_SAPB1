# BADivationAlertLevelEnum — Nivel de alerta por desviación del acuerdo global

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BADivationAlertLevelEnum`
- **Descripción (ES):** Nivel de alerta por desviación del acuerdo global
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `badal_NoWarning` | 0 | Number Warning | Sin advertencia |
| `badal_Warning` | 1 | Warning | Advertencia |
| `badal_Block` | 2 | Block | Bloquear |

## Used by (3 properties)

- [AdminInfo](../Tipos-Complejos/AdminInfo.md).`ActionWhenDeviateFromBAForAccounting`
- [AdminInfo](../Tipos-Complejos/AdminInfo.md).`ActionWhenDeviateFromBAForGRPO`
- [AdminInfo](../Tipos-Complejos/AdminInfo.md).`ActionWhenDeviateFromBAForPO`
