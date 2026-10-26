# NCMCodesSetupService — Servicio de configuración de códigos NCM

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `NCMCodesSetupService`
- **Descripción (ES):** Servicio de configuración de códigos NCM
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`NCMCodesSetupService_GetNCMCodeSetupList`](#ncmcodessetupservice_getncmcodesetuplist) | action | Collection([NCMCodeSetupParams](../Tipos-Complejos/NCMCodeSetupParams.md)) | Get NCM Code Setup List | Obtener lista de configuración de códigos NCM |

## NCMCodesSetupService_GetNCMCodeSetupList

- **Descripción (ES):** Obtener lista de configuración de códigos NCM
- **Request:** `POST /b1s/v2/NCMCodesSetupService_GetNCMCodeSetupList`
- **Parameters:** none
- **Returns:** Collection([NCMCodeSetupParams](../Tipos-Complejos/NCMCodeSetupParams.md))

