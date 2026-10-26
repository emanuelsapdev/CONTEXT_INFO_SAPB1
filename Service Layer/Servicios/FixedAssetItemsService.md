# FixedAssetItemsService — Servicio de artículos de activos fijos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `FixedAssetItemsService`
- **Descripción (ES):** Servicio de artículos de activos fijos
- **Operations:** 3

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`FixedAssetItemsService_GetAssetEndBalance`](#fixedassetitemsservice_getassetendbalance) | action | [FixedAssetEndBalance](../Tipos-Complejos/FixedAssetEndBalance.md) | Get Asset End Balance | Obtener saldo final del activo |
| [`FixedAssetItemsService_GetAssetValuesList`](#fixedassetitemsservice_getassetvalueslist) | action | Collection([FixedAssetValues](../Tipos-Complejos/FixedAssetValues.md)) | Get Asset Values List | Obtener lista de valores de activos |
| [`FixedAssetItemsService_UpdateAssetEndBalance`](#fixedassetitemsservice_updateassetendbalance) | action | — | Update Asset End Balance | Actualizar saldo final del activo |

## FixedAssetItemsService_GetAssetEndBalance

- **Descripción (ES):** Obtener saldo final del activo
- **Request:** `POST /b1s/v2/FixedAssetItemsService_GetAssetEndBalance`
- **Parameters:** `FixedAssetValuesParams` ([FixedAssetValuesParams](../Tipos-Complejos/FixedAssetValuesParams.md))
- **Returns:** [FixedAssetEndBalance](../Tipos-Complejos/FixedAssetEndBalance.md)

```json
{
  "FixedAssetValuesParams": {
    "ItemCode": "string",
    "FiscalYear": "string",
    "DepreciationArea": "string"
  }
}
```

## FixedAssetItemsService_GetAssetValuesList

- **Descripción (ES):** Obtener lista de valores de activos
- **Request:** `POST /b1s/v2/FixedAssetItemsService_GetAssetValuesList`
- **Parameters:** `FixedAssetValuesParams` ([FixedAssetValuesParams](../Tipos-Complejos/FixedAssetValuesParams.md))
- **Returns:** Collection([FixedAssetValues](../Tipos-Complejos/FixedAssetValues.md))

```json
{
  "FixedAssetValuesParams": {
    "ItemCode": "string",
    "FiscalYear": "string",
    "DepreciationArea": "string"
  }
}
```

## FixedAssetItemsService_UpdateAssetEndBalance

- **Descripción (ES):** Actualizar saldo final del activo
- **Request:** `POST /b1s/v2/FixedAssetItemsService_UpdateAssetEndBalance`
- **Parameters:** `FixedAssetValuesParams` ([FixedAssetValuesParams](../Tipos-Complejos/FixedAssetValuesParams.md)), `FixedAssetEndBalance` ([FixedAssetEndBalance](../Tipos-Complejos/FixedAssetEndBalance.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "FixedAssetValuesParams": {
    "ItemCode": "string",
    "FiscalYear": "string",
    "DepreciationArea": "string"
  },
  "FixedAssetEndBalance": {
    "HistoricalAPC": 0.0,
    "AcquisitionCost": 0.0,
    "NetBookValue": 0.0,
    "HistoricalNBV": 0.0,
    ...
  }
}
```

