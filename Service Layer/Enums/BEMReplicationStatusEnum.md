# BEMReplicationStatusEnum — Estado de replicación BEM

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BEMReplicationStatusEnum`
- **Descripción (ES):** Estado de replicación BEM
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bemStatus_New` | 0 | Bem Status New | Nuevo |
| `bemStatus_Initializing` | 1 | Bem Status Initializing | Inicializando |
| `bemStatus_InProcess` | 2 | Bem Status In Process | En proceso |
| `bemStatus_Complete` | 3 | Bem Status Complete | Completado |
| `bemStatus_CompleteWithInconsistencies` | 4 | Bem Status Complete With Inconsistencies | Completado con inconsistencias |
| `bemStatus_Error` | 5 | Bem Status Error | Error |

## Used by (1 properties)

- [BEMReplicationPeriod](../Entidades/BEMReplicationPeriods.md).`Status`
