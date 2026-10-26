# DNFCodeSetupService — Servicio de configuración de códigos DNF

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `DNFCodeSetupService`
- **Descripción (ES):** Servicio de configuración de códigos DNF
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`DNFCodeSetupService_GetDNFCodeSetupList`](#dnfcodesetupservice_getdnfcodesetuplist) | action | Collection([DNFCodeSetupParams](../Tipos-Complejos/DNFCodeSetupParams.md)) | Get DNF Code Setup List | Obtener lista de configuración de códigos DNF |

## DNFCodeSetupService_GetDNFCodeSetupList

- **Descripción (ES):** Obtener lista de configuración de códigos DNF
- **Request:** `POST /b1s/v2/DNFCodeSetupService_GetDNFCodeSetupList`
- **Parameters:** none
- **Returns:** Collection([DNFCodeSetupParams](../Tipos-Complejos/DNFCodeSetupParams.md))

