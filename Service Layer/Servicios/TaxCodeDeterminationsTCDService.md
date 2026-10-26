# TaxCodeDeterminationsTCDService — Servicio de determinación de indicadores de impuestos (TCD)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `TaxCodeDeterminationsTCDService`
- **Descripción (ES):** Servicio de determinación de indicadores de impuestos (TCD)
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`TaxCodeDeterminationsTCDService_GetTaxCodeDeterminationTCDList`](#taxcodedeterminationstcdservice_gettaxcodedeterminationtcdlist) | action | Collection([TaxCodeDeterminationTCDParams](../Tipos-Complejos/TaxCodeDeterminationTCDParams.md)) | Get Tax Code Determination TCD List | Obtener lista de determinación de indicadores de impuestos (TCD) |

## TaxCodeDeterminationsTCDService_GetTaxCodeDeterminationTCDList

- **Descripción (ES):** Obtener lista de determinación de indicadores de impuestos (TCD)
- **Request:** `POST /b1s/v2/TaxCodeDeterminationsTCDService_GetTaxCodeDeterminationTCDList`
- **Parameters:** none
- **Returns:** Collection([TaxCodeDeterminationTCDParams](../Tipos-Complejos/TaxCodeDeterminationTCDParams.md))

