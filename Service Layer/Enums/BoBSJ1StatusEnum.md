# BoBSJ1StatusEnum — Estado de subtarea de planificación en segundo plano

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoBSJ1StatusEnum`
- **Descripción (ES):** Estado de subtarea de planificación en segundo plano
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bobsj1Scheduled` | 0 | Bobsj 1 Scheduled | Programada |
| `bobsj1Running` | 1 | Bobsj 1 Running | En ejecución |
| `bobsj1Error` | 2 | Bobsj 1 Error | Error |
| `bobsj1Finished` | 3 | Bobsj 1 Finished | Finalizada |
| `bobsj1Pending` | 4 | Bobsj 1 Pending | Pendiente |
| `bobsj1Creating` | 5 | Bobsj 1 Creating | Creando |

## Used by (1 properties)

- [BackendSchedulingSubTasks](../Tipos-Complejos/BackendSchedulingSubTasks.md).`Status`
