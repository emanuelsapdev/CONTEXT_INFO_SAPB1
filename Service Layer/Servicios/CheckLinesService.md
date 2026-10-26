# CheckLinesService — Servicio de líneas de cheques

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `CheckLinesService`
- **Descripción (ES):** Servicio de líneas de cheques
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`CheckLinesService_GetCheckLine`](#checklinesservice_getcheckline) | action | [CheckLine](../Tipos-Complejos/CheckLine.md) | Get Check Line | Obtener línea de cheque |
| [`CheckLinesService_GetValidCheckLineList`](#checklinesservice_getvalidchecklinelist) | action | Collection([CheckLineParams](../Tipos-Complejos/CheckLineParams.md)) | Get Valid Check Line List | Obtener lista de líneas de cheque válidas |

## CheckLinesService_GetCheckLine

- **Descripción (ES):** Obtener línea de cheque
- **Request:** `POST /b1s/v2/CheckLinesService_GetCheckLine`
- **Parameters:** `CheckLineParams` ([CheckLineParams](../Tipos-Complejos/CheckLineParams.md))
- **Returns:** [CheckLine](../Tipos-Complejos/CheckLine.md)

```json
{
  "CheckLineParams": {
    "CheckKey": 0
  }
}
```

## CheckLinesService_GetValidCheckLineList

- **Descripción (ES):** Obtener lista de líneas de cheque válidas
- **Request:** `POST /b1s/v2/CheckLinesService_GetValidCheckLineList`
- **Parameters:** none
- **Returns:** Collection([CheckLineParams](../Tipos-Complejos/CheckLineParams.md))

