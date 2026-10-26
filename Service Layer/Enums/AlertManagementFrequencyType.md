# AlertManagementFrequencyType — Tipo de frecuencia de alertas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `AlertManagementFrequencyType`
- **Descripción (ES):** Tipo de frecuencia de alertas
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `atfi_Minutes` | 0 | Minutes | Minutos |
| `atfi_Hours` | 1 | Hours | Horas |
| `atfi_Days` | 2 | Days | Días |
| `atfi_Weeks` | 3 | Weeks | Semanas |
| `atfi_Monthly` | 4 | Monthly | Mensual |

## Used by (1 properties)

- [AlertManagement](../Entidades/AlertManagements.md).`FrequencyType`
