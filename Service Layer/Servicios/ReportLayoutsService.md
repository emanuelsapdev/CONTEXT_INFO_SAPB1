# ReportLayoutsService — Servicio de formatos de informe

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ReportLayoutsService`
- **Descripción (ES):** Servicio de formatos de informe
- **Operations:** 11

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ReportLayoutsService_AddReportLayout`](#reportlayoutsservice_addreportlayout) | action | [ReportLayoutParams](../Tipos-Complejos/ReportLayoutParams.md) | Add Report Layout | Agregar formato de informe |
| [`ReportLayoutsService_AddReportLayoutToMenu`](#reportlayoutsservice_addreportlayouttomenu) | action | [ReportLayoutParams](../Tipos-Complejos/ReportLayoutParams.md) | Add Report Layout To Menu | Agregar formato de informe al menú |
| [`ReportLayoutsService_DeleteReportLayout`](#reportlayoutsservice_deletereportlayout) | action | — | Delete Report Layout | Eliminar formato de informe |
| [`ReportLayoutsService_DeleteReportLayoutAndMenu`](#reportlayoutsservice_deletereportlayoutandmenu) | action | — | Delete Report Layout And Menu | Eliminar formato de informe y menú |
| [`ReportLayoutsService_GetDefaultReport`](#reportlayoutsservice_getdefaultreport) | action | [DefaultReportParams](../Tipos-Complejos/DefaultReportParams.md) | Get Default Report | Obtener informe predeterminado |
| [`ReportLayoutsService_GetDefaultReportLayout`](#reportlayoutsservice_getdefaultreportlayout) | action | [ReportLayout](../Tipos-Complejos/ReportLayout.md) | Get Default Report Layout | Obtener formato de informe predeterminado |
| [`ReportLayoutsService_GetReportLayout`](#reportlayoutsservice_getreportlayout) | action | [ReportLayout](../Tipos-Complejos/ReportLayout.md) | Get Report Layout | Obtener formato de informe |
| [`ReportLayoutsService_GetReportLayoutList`](#reportlayoutsservice_getreportlayoutlist) | action | Collection([ReportLayoutParams](../Tipos-Complejos/ReportLayoutParams.md)) | Get Report Layout List | Obtener lista de formatos de informe |
| [`ReportLayoutsService_SetDefaultReport`](#reportlayoutsservice_setdefaultreport) | action | — | Set Default Report | Establecer informe predeterminado |
| [`ReportLayoutsService_UpdateLanguageReport`](#reportlayoutsservice_updatelanguagereport) | action | — | Update Language Report | Actualizar informe de idioma |
| [`ReportLayoutsService_UpdatePrinterSettings`](#reportlayoutsservice_updateprintersettings) | action | — | Update Printer Settings | Actualizar configuración de impresora |

## ReportLayoutsService_AddReportLayout

- **Descripción (ES):** Agregar formato de informe
- **Request:** `POST /b1s/v2/ReportLayoutsService_AddReportLayout`
- **Parameters:** `ReportLayout` ([ReportLayout](../Tipos-Complejos/ReportLayout.md))
- **Returns:** [ReportLayoutParams](../Tipos-Complejos/ReportLayoutParams.md)

```json
{
  "ReportLayout": {
    "Name": "string",
    "Author": "string",
    "Remarks": "string",
    "Width": 0,
    ...
  }
}
```

## ReportLayoutsService_AddReportLayoutToMenu

- **Descripción (ES):** Agregar formato de informe al menú
- **Request:** `POST /b1s/v2/ReportLayoutsService_AddReportLayoutToMenu`
- **Parameters:** `ReportLayout` ([ReportLayout](../Tipos-Complejos/ReportLayout.md)), `ReportInputParams` ([ReportInputParams](../Tipos-Complejos/ReportInputParams.md))
- **Returns:** [ReportLayoutParams](../Tipos-Complejos/ReportLayoutParams.md)

```json
{
  "ReportLayout": {
    "Name": "string",
    "Author": "string",
    "Remarks": "string",
    "Width": 0,
    ...
  },
  "ReportInputParams": {
    "ReportLayoutMenuID": "string"
  }
}
```

## ReportLayoutsService_DeleteReportLayout

- **Descripción (ES):** Eliminar formato de informe
- **Request:** `POST /b1s/v2/ReportLayoutsService_DeleteReportLayout`
- **Parameters:** `ReportLayoutParams` ([ReportLayoutParams](../Tipos-Complejos/ReportLayoutParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ReportLayoutParams": {
    "LayoutCode": "string",
    "LayoutName": "string",
    ...
  }
}
```

## ReportLayoutsService_DeleteReportLayoutAndMenu

- **Descripción (ES):** Eliminar formato de informe y menú
- **Request:** `POST /b1s/v2/ReportLayoutsService_DeleteReportLayoutAndMenu`
- **Parameters:** `ReportLayoutParams` ([ReportLayoutParams](../Tipos-Complejos/ReportLayoutParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ReportLayoutParams": {
    "LayoutCode": "string",
    "LayoutName": "string",
    ...
  }
}
```

## ReportLayoutsService_GetDefaultReport

- **Descripción (ES):** Obtener informe predeterminado
- **Request:** `POST /b1s/v2/ReportLayoutsService_GetDefaultReport`
- **Parameters:** `ReportParams` ([ReportParams](../Tipos-Complejos/ReportParams.md))
- **Returns:** [DefaultReportParams](../Tipos-Complejos/DefaultReportParams.md)

```json
{
  "ReportParams": {
    "ReportCode": "string",
    "UserID": 0,
    "CardCode": "string"
  }
}
```

## ReportLayoutsService_GetDefaultReportLayout

- **Descripción (ES):** Obtener formato de informe predeterminado
- **Request:** `POST /b1s/v2/ReportLayoutsService_GetDefaultReportLayout`
- **Parameters:** `ReportParams` ([ReportParams](../Tipos-Complejos/ReportParams.md))
- **Returns:** [ReportLayout](../Tipos-Complejos/ReportLayout.md)

```json
{
  "ReportParams": {
    "ReportCode": "string",
    "UserID": 0,
    "CardCode": "string"
  }
}
```

## ReportLayoutsService_GetReportLayout

- **Descripción (ES):** Obtener formato de informe
- **Request:** `POST /b1s/v2/ReportLayoutsService_GetReportLayout`
- **Parameters:** `ReportLayoutParams` ([ReportLayoutParams](../Tipos-Complejos/ReportLayoutParams.md))
- **Returns:** [ReportLayout](../Tipos-Complejos/ReportLayout.md)

```json
{
  "ReportLayoutParams": {
    "LayoutCode": "string",
    "LayoutName": "string",
    ...
  }
}
```

## ReportLayoutsService_GetReportLayoutList

- **Descripción (ES):** Obtener lista de formatos de informe
- **Request:** `POST /b1s/v2/ReportLayoutsService_GetReportLayoutList`
- **Parameters:** `ReportParams` ([ReportParams](../Tipos-Complejos/ReportParams.md))
- **Returns:** Collection([ReportLayoutParams](../Tipos-Complejos/ReportLayoutParams.md))

```json
{
  "ReportParams": {
    "ReportCode": "string",
    "UserID": 0,
    "CardCode": "string"
  }
}
```

## ReportLayoutsService_SetDefaultReport

- **Descripción (ES):** Establecer informe predeterminado
- **Request:** `POST /b1s/v2/ReportLayoutsService_SetDefaultReport`
- **Parameters:** `DefaultReportParams` ([DefaultReportParams](../Tipos-Complejos/DefaultReportParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "DefaultReportParams": {
    "ReportCode": "string",
    "LayoutCode": "string",
    "UserID": 0,
    "CardCode": "string"
  }
}
```

## ReportLayoutsService_UpdateLanguageReport

- **Descripción (ES):** Actualizar informe de idioma
- **Request:** `POST /b1s/v2/ReportLayoutsService_UpdateLanguageReport`
- **Parameters:** `ReportLayout` ([ReportLayout](../Tipos-Complejos/ReportLayout.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ReportLayout": {
    "Name": "string",
    "Author": "string",
    "Remarks": "string",
    "Width": 0,
    ...
  }
}
```

## ReportLayoutsService_UpdatePrinterSettings

- **Descripción (ES):** Actualizar configuración de impresora
- **Request:** `POST /b1s/v2/ReportLayoutsService_UpdatePrinterSettings`
- **Parameters:** `ReportLayout` ([ReportLayout](../Tipos-Complejos/ReportLayout.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ReportLayout": {
    "Name": "string",
    "Author": "string",
    "Remarks": "string",
    "Width": 0,
    ...
  }
}
```

