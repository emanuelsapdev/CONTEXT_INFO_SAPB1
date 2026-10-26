# AlternativeItemsService — Servicio de artículos alternativos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `AlternativeItemsService`
- **Descripción (ES):** Servicio de artículos alternativos
- **Operations:** 4

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`AlternativeItemsService_AddItem`](#alternativeitemsservice_additem) | action | [OriginalItemParams](../Tipos-Complejos/OriginalItemParams.md) | Add Item | Agregar elemento |
| [`AlternativeItemsService_DeleteItem`](#alternativeitemsservice_deleteitem) | action | — | Delete Item | Eliminar elemento |
| [`AlternativeItemsService_GetItem`](#alternativeitemsservice_getitem) | action | [OriginalItem](../Tipos-Complejos/OriginalItem.md) | Get Item | Obtener elemento |
| [`AlternativeItemsService_UpdateItem`](#alternativeitemsservice_updateitem) | action | — | Update Item | Actualizar elemento |

## AlternativeItemsService_AddItem

- **Descripción (ES):** Agregar elemento
- **Request:** `POST /b1s/v2/AlternativeItemsService_AddItem`
- **Parameters:** `OriginalItem` ([OriginalItem](../Tipos-Complejos/OriginalItem.md))
- **Returns:** [OriginalItemParams](../Tipos-Complejos/OriginalItemParams.md)

```json
{
  "OriginalItem": {
    "ItemCode": "string",
    "ItemName": "string",
    ...
  }
}
```

## AlternativeItemsService_DeleteItem

- **Descripción (ES):** Eliminar elemento
- **Request:** `POST /b1s/v2/AlternativeItemsService_DeleteItem`
- **Parameters:** `OriginalItemParams` ([OriginalItemParams](../Tipos-Complejos/OriginalItemParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "OriginalItemParams": {
    "ItemCode": "string",
    "ItemName": "string"
  }
}
```

## AlternativeItemsService_GetItem

- **Descripción (ES):** Obtener elemento
- **Request:** `POST /b1s/v2/AlternativeItemsService_GetItem`
- **Parameters:** `OriginalItemParams` ([OriginalItemParams](../Tipos-Complejos/OriginalItemParams.md))
- **Returns:** [OriginalItem](../Tipos-Complejos/OriginalItem.md)

```json
{
  "OriginalItemParams": {
    "ItemCode": "string",
    "ItemName": "string"
  }
}
```

## AlternativeItemsService_UpdateItem

- **Descripción (ES):** Actualizar elemento
- **Request:** `POST /b1s/v2/AlternativeItemsService_UpdateItem`
- **Parameters:** `OriginalItem` ([OriginalItem](../Tipos-Complejos/OriginalItem.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "OriginalItem": {
    "ItemCode": "string",
    "ItemName": "string",
    ...
  }
}
```

