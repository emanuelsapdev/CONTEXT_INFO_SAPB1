# InventoryPostingsService — Servicio de contabilizaciones de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `InventoryPostingsService`
- **Descripción (ES):** Servicio de contabilizaciones de inventario
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`InventoryPostingsService_GetList`](#inventorypostingsservice_getlist) | action | Collection([InventoryPostingParams](../Tipos-Complejos/InventoryPostingParams.md)) | Get List | Obtener lista |
| [`InventoryPostingsService_SetCopyOption`](#inventorypostingsservice_setcopyoption) | action | — | Set Copy Option | Establecer opción de copia |

## InventoryPostingsService_GetList

- **Descripción (ES):** Obtener lista
- **Request:** `POST /b1s/v2/InventoryPostingsService_GetList`
- **Parameters:** none
- **Returns:** Collection([InventoryPostingParams](../Tipos-Complejos/InventoryPostingParams.md))

## InventoryPostingsService_SetCopyOption

- **Descripción (ES):** Establecer opción de copia
- **Request:** `POST /b1s/v2/InventoryPostingsService_SetCopyOption`
- **Parameters:** `InventoryPostingCopyOption` ([InventoryPostingCopyOption](../Tipos-Complejos/InventoryPostingCopyOption.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "InventoryPostingCopyOption": {
    "BaseEntry": 0,
    ...
  }
}
```

