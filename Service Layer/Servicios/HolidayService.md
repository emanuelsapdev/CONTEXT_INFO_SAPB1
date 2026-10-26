# HolidayService — Servicio de días festivos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `HolidayService`
- **Descripción (ES):** Servicio de días festivos
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`HolidayService_GetHolidayList`](#holidayservice_getholidaylist) | action | Collection([HolidayParams](../Tipos-Complejos/HolidayParams.md)) | Get Holiday List | Obtener lista de días festivos |

## HolidayService_GetHolidayList

- **Descripción (ES):** Obtener lista de días festivos
- **Request:** `POST /b1s/v2/HolidayService_GetHolidayList`
- **Parameters:** none
- **Returns:** Collection([HolidayParams](../Tipos-Complejos/HolidayParams.md))

