# AssetManualDepreciationService — Servicio de amortización manual de activos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `AssetManualDepreciationService`
- **Descripción (ES):** Servicio de amortización manual de activos
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`AssetManualDepreciationService_Cancel`](#assetmanualdepreciationservice_cancel) | action | — | Cancel | Cancelar |
| [`AssetManualDepreciationService_GetList`](#assetmanualdepreciationservice_getlist) | action | Collection([AssetDocumentParams](../Tipos-Complejos/AssetDocumentParams.md)) | Get List | Obtener lista |

## AssetManualDepreciationService_Cancel

- **Descripción (ES):** Cancelar
- **Request:** `POST /b1s/v2/AssetManualDepreciationService_Cancel`
- **Parameters:** `AssetDocumentParams` ([AssetDocumentParams](../Tipos-Complejos/AssetDocumentParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "AssetDocumentParams": {
    "DocEntry": 0,
    "CancellationDate": "2026-01-31",
    ...
  }
}
```

## AssetManualDepreciationService_GetList

- **Descripción (ES):** Obtener lista
- **Request:** `POST /b1s/v2/AssetManualDepreciationService_GetList`
- **Parameters:** none
- **Returns:** Collection([AssetDocumentParams](../Tipos-Complejos/AssetDocumentParams.md))

