# ActivitySubjectService — Servicio de asuntos de actividades

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ActivitySubjectService`
- **Descripción (ES):** Servicio de asuntos de actividades
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ActivitySubjectService_GetActivitySubjectList`](#activitysubjectservice_getactivitysubjectlist) | action | Collection([ActivitySubjectParams](../Tipos-Complejos/ActivitySubjectParams.md)) | Get Activity Subject List | Obtener lista de asuntos de actividades |
| [`ActivitySubjectService_GetListByTypeCode`](#activitysubjectservice_getlistbytypecode) | action | Collection([ActivitySubjectParams](../Tipos-Complejos/ActivitySubjectParams.md)) | Get List By Type Code | Obtener lista por código de tipo |

## ActivitySubjectService_GetActivitySubjectList

- **Descripción (ES):** Obtener lista de asuntos de actividades
- **Request:** `POST /b1s/v2/ActivitySubjectService_GetActivitySubjectList`
- **Parameters:** none
- **Returns:** Collection([ActivitySubjectParams](../Tipos-Complejos/ActivitySubjectParams.md))

## ActivitySubjectService_GetListByTypeCode

- **Descripción (ES):** Obtener lista por código de tipo
- **Request:** `POST /b1s/v2/ActivitySubjectService_GetListByTypeCode`
- **Parameters:** `ActivitySubject` ([ActivitySubject](../Entidades/ActivitySubjects.md))
- **Returns:** Collection([ActivitySubjectParams](../Tipos-Complejos/ActivitySubjectParams.md))

```json
{
  "ActivitySubject": {
    "Code": 0,
    "Description": "string",
    "ActivityType": 0,
    ...
  }
}
```

