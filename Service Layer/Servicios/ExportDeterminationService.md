# ExportDeterminationService — Servicio de determinaciones de exportación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ExportDeterminationService`
- **Descripción (ES):** Servicio de determinaciones de exportación
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ExportDeterminationService_GetDeterminations`](#exportdeterminationservice_getdeterminations) | action | Collection([ExportDetermination](../Entidades/ExportDeterminations.md)) | Get Determinations | Obtener determinaciones |

## ExportDeterminationService_GetDeterminations

- **Descripción (ES):** Obtener determinaciones
- **Request:** `POST /b1s/v2/ExportDeterminationService_GetDeterminations`
- **Parameters:** `ExportDeterminationsParams` ([ExportDeterminationsParams](../Tipos-Complejos/ExportDeterminationsParams.md))
- **Returns:** Collection([ExportDetermination](../Entidades/ExportDeterminations.md))

```json
{
  "ExportDeterminationsParams": { }
}
```

