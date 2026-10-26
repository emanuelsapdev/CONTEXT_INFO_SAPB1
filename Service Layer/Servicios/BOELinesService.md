# BOELinesService — Servicio de líneas de letras de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `BOELinesService`
- **Descripción (ES):** Servicio de líneas de letras de cambio
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`BOELinesService_GetBOELine`](#boelinesservice_getboeline) | action | [BOELine](../Tipos-Complejos/BOELine.md) | Get BOE Line | Obtener línea de letra de cambio |

## BOELinesService_GetBOELine

- **Descripción (ES):** Obtener línea de letra de cambio
- **Request:** `POST /b1s/v2/BOELinesService_GetBOELine`
- **Parameters:** `BOELineParams` ([BOELineParams](../Tipos-Complejos/BOELineParams.md))
- **Returns:** [BOELine](../Tipos-Complejos/BOELine.md)

```json
{
  "BOELineParams": {
    "BOEKey": 0
  }
}
```

