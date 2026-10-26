# CockpitsService — Servicio de cockpits

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `CockpitsService`
- **Descripción (ES):** Servicio de cockpits
- **Operations:** 4

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`CockpitsService_GetCockpitList`](#cockpitsservice_getcockpitlist) | action | Collection([CockpitParams](../Tipos-Complejos/CockpitParams.md)) | Get Cockpit List | Obtener lista de cockpits |
| [`CockpitsService_GetTemplateCockpitList`](#cockpitsservice_gettemplatecockpitlist) | action | Collection([CockpitParams](../Tipos-Complejos/CockpitParams.md)) | Get Template Cockpit List | Obtener lista de cockpits de plantilla |
| [`CockpitsService_GetUserCockpitList`](#cockpitsservice_getusercockpitlist) | action | Collection([CockpitParams](../Tipos-Complejos/CockpitParams.md)) | Get User Cockpit List | Obtener lista de cockpits de usuario |
| [`CockpitsService_PublishCockpit`](#cockpitsservice_publishcockpit) | action | — | Publish Cockpit | Publicar cockpit |

## CockpitsService_GetCockpitList

- **Descripción (ES):** Obtener lista de cockpits
- **Request:** `POST /b1s/v2/CockpitsService_GetCockpitList`
- **Parameters:** none
- **Returns:** Collection([CockpitParams](../Tipos-Complejos/CockpitParams.md))

## CockpitsService_GetTemplateCockpitList

- **Descripción (ES):** Obtener lista de cockpits de plantilla
- **Request:** `POST /b1s/v2/CockpitsService_GetTemplateCockpitList`
- **Parameters:** none
- **Returns:** Collection([CockpitParams](../Tipos-Complejos/CockpitParams.md))

## CockpitsService_GetUserCockpitList

- **Descripción (ES):** Obtener lista de cockpits de usuario
- **Request:** `POST /b1s/v2/CockpitsService_GetUserCockpitList`
- **Parameters:** none
- **Returns:** Collection([CockpitParams](../Tipos-Complejos/CockpitParams.md))

## CockpitsService_PublishCockpit

- **Descripción (ES):** Publicar cockpit
- **Request:** `POST /b1s/v2/CockpitsService_PublishCockpit`
- **Parameters:** `Cockpit` ([Cockpit](../Entidades/Cockpits.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "Cockpit": {
    "AbsEntry": 0,
    "Code": 0,
    "Name": "string",
    "Description": "string",
    ...
  }
}
```

