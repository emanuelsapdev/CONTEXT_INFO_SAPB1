# FinancialYearsService — Servicio de ejercicios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `FinancialYearsService`
- **Descripción (ES):** Servicio de ejercicios
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`FinancialYearsService_GetFinancialYearList`](#financialyearsservice_getfinancialyearlist) | action | Collection([FinancialYearParams](../Tipos-Complejos/FinancialYearParams.md)) | Get Financial Year List | Obtener lista de ejercicios |

## FinancialYearsService_GetFinancialYearList

- **Descripción (ES):** Obtener lista de ejercicios
- **Request:** `POST /b1s/v2/FinancialYearsService_GetFinancialYearList`
- **Parameters:** none
- **Returns:** Collection([FinancialYearParams](../Tipos-Complejos/FinancialYearParams.md))

