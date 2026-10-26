# ServiceCallActivity — Actividad de la llamada de servicio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ServiceCallActivity`
- **Descripción (ES):** Actividad de la llamada de servicio
- **Description (EN):** Service Call Activity
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `ActivityCode` | Edm.Int32 | Yes | Activity Code | Código de actividad |

## Used by (properties)

- [ServiceCall](../Entidades/ServiceCalls.md).`ServiceCallActivities`
