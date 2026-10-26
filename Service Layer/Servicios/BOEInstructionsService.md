# BOEInstructionsService — Servicio de instrucciones de letras de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `BOEInstructionsService`
- **Descripción (ES):** Servicio de instrucciones de letras de cambio
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`BOEInstructionsService_GetBOEInstructionList`](#boeinstructionsservice_getboeinstructionlist) | action | Collection([BOEInstructionParams](../Tipos-Complejos/BOEInstructionParams.md)) | Get BOE Instruction List | Obtener lista de instrucciones de letras de cambio |

## BOEInstructionsService_GetBOEInstructionList

- **Descripción (ES):** Obtener lista de instrucciones de letras de cambio
- **Request:** `POST /b1s/v2/BOEInstructionsService_GetBOEInstructionList`
- **Parameters:** none
- **Returns:** Collection([BOEInstructionParams](../Tipos-Complejos/BOEInstructionParams.md))

