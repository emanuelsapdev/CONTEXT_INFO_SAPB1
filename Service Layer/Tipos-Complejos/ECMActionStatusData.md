# ECMActionStatusData — Datos de estado de acción ECM

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ECMActionStatusData`
- **Descripción (ES):** Datos de estado de acción ECM
- **Description (EN):** ECM Action Status Data

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `ActStatus` | [EcmActionStatusEnum](../Enums/EcmActionStatusEnum.md) | Yes | Act Status | Estado de actividad |
| 3 | `ReportID` | Edm.String | Yes | Report ID | ID de informe |
| 4 | `ReceivDate` | Edm.DateTimeOffset | Yes | Receiv Date | Fecha de recepción |
| 5 | `ActMessage` | Edm.String | Yes | Act Message | Mensaje de actividad |

## Used by (service operations)

- [`ElectronicCommunicationActionService_GetAction`](../Servicios/ElectronicCommunicationActionService.md#electroniccommunicationactionservice_getaction)
- [`ElectronicCommunicationActionService_UpdateAction`](../Servicios/ElectronicCommunicationActionService.md#electroniccommunicationactionservice_updateaction)
