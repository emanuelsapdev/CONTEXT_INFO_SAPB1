# PickListsService — Servicio de listas de picking

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `PickListsService`
- **Descripción (ES):** Servicio de listas de picking
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`PickListsService_Close`](#picklistsservice_close) | action | — | Close | Cerrar |
| [`PickListsService_UpdateReleasedAllocation`](#picklistsservice_updatereleasedallocation) | action | — | Update Released Allocation | Actualizar asignación liberada |

## PickListsService_Close

- **Descripción (ES):** Cerrar
- **Request:** `POST /b1s/v2/PickListsService_Close`
- **Parameters:** `PickList` ([PickList](../Entidades/PickLists.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PickList": {
    "Absoluteentry": 0,
    "Name": "string",
    "OwnerCode": 0,
    "OwnerName": "string",
    ...
  }
}
```

## PickListsService_UpdateReleasedAllocation

- **Descripción (ES):** Actualizar asignación liberada
- **Request:** `POST /b1s/v2/PickListsService_UpdateReleasedAllocation`
- **Parameters:** `PickList` ([PickList](../Entidades/PickLists.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PickList": {
    "Absoluteentry": 0,
    "Name": "string",
    "OwnerCode": 0,
    "OwnerName": "string",
    ...
  }
}
```

