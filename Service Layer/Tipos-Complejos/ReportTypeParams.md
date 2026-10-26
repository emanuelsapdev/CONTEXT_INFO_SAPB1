# ReportTypeParams — Parámetros de tipos de informe

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ReportTypeParams`
- **Descripción (ES):** Parámetros de tipos de informe
- **Description (EN):** Report Type Parameters

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TypeCode` | Edm.String | Yes | Type Code | Código de tipo |
| 2 | `TypeName` | Edm.String | Yes | Type Name | Nombre del tipo |
| 3 | `AddonName` | Edm.String | Yes | Addon Name | Nombre del add-on |
| 4 | `AddonFormType` | Edm.String | Yes | Addon Form Type | Tipo de formulario del add-on |
| 5 | `MenuID` | Edm.String | Yes | Menu ID | ID de menú |

## Used by (service operations)

- [`ReportTypesService_GetReportTypeList`](../Servicios/ReportTypesService.md#reporttypesservice_getreporttypelist)
