# PM_TimeSheetLineData — Gestión de proyectos - Línea de hoja de horas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PM_TimeSheetLineData`
- **Descripción (ES):** Gestión de proyectos - Línea de hoja de horas
- **Description (EN):** PM Time Sheet Line Data
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 21

## Properties (21)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineID` | Edm.Int32 | Yes | Line ID | ID de línea |
| 2 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 3 | `ActivityType` | Edm.Int32 | Yes | Activity Type | Tipo de actividad |
| 4 | `LaborItem` | Edm.String | Yes | Labor Item | Artículo de mano de obra |
| 5 | `StartTime` | Edm.TimeOfDay | Yes | Start Time | Hora de inicio |
| 6 | `EndTime` | Edm.TimeOfDay | Yes | End Time | Hora de fin |
| 7 | `Workorder` | Edm.Int32 | Yes | Workorder | Orden de trabajo |
| 8 | `ServiceCall` | Edm.Int32 | Yes | Service Call | Llamada de servicio |
| 9 | `CostCenter` | Edm.String | Yes | Cost Center | Centro de costo |
| 10 | `FinancialProject` | Edm.String | Yes | Financial Project | Proyecto financiero |
| 11 | `Location` | Edm.Int32 | Yes | Location | Ubicación |
| 12 | `GPSData` | Edm.String | Yes | GPS Data | Datos GPS |
| 13 | `Branch` | Edm.Int32 | Yes | Branch | Sucursal |
| 14 | `Break` | Edm.TimeOfDay | Yes | Break | Corte/salto |
| 15 | `NonBillableTime` | Edm.TimeOfDay | Yes | Non Billable Time | Tiempo no facturable |
| 16 | `EffectiveTime` | Edm.TimeOfDay | Yes | Effective Time | Hora de vigencia |
| 17 | `BillableTime` | Edm.TimeOfDay | Yes | Billable Time | Tiempo facturable |
| 18 | `FullDay` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Full Day | Día completo |
| 19 | `ProjectID` | Edm.Int32 | Yes | Project ID | ID de proyecto |
| 20 | `SubprojectID` | Edm.Int32 | Yes | Subproject ID | ID del subproyecto |
| 21 | `StageID` | Edm.Int32 | Yes | Stage ID | ID de etapa |

## Used by (properties)

- [PM_TimeSheetData](../Entidades/ProjectManagementTimeSheet.md).`PM_TimeSheetLineDataCollection`
