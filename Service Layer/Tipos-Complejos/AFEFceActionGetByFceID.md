# AFEFceActionGetByFceID — [Loc. AR] Acción FCE por ID de FCE

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AFEFceActionGetByFceID`
- **Descripción (ES):** [Loc. AR] Acción FCE por ID de FCE
- **Description (EN):** AFE Fce Action Get By Fce ID

- **Properties:** 16

## Properties (16)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `SrcObjType` | Edm.String | Yes | Src Obj Type | Tipo de objeto de origen |
| 2 | `DocSubType` | Edm.String | Yes | Document Sub Type | Subtipo de documento |
| 3 | `SrcObjAbs` | Edm.Int32 | Yes | Src Obj Abs | Entrada del objeto de origen |
| 4 | `AssignedID` | Edm.String | Yes | Assigned ID | ID asignado |
| 5 | `FCE_ID` | Edm.Int32 | Yes | FCE ID | ID FCE |
| 6 | `FCE_TotalVal` | Edm.Double | Yes | FCE Total Val | Valor total FCE |
| 7 | `FCE_Currency` | Edm.String | Yes | FCE Currency | Moneda FCE |
| 8 | `FCE_DcApStat` | Edm.String | Yes | FCE Dc Ap Stat | Estado de aceptación del documento FCE |
| 9 | `ActStatus` | [EcmActionStatusEnum](../Enums/EcmActionStatusEnum.md) | Yes | Act Status | Estado de actividad |
| 10 | `FCE_DocType` | Edm.Int32 | Yes | FCE Document Type | Tipo de documento FCE |
| 11 | `FCE_POI` | Edm.String | Yes | FCE POI | Punto de emisión FCE |
| 12 | `FCE_Folio` | Edm.Int32 | Yes | FCE Folio | Folio FCE |
| 13 | `FCE_RjRsnCod` | Edm.String | Yes | FCE Rj Rsn Cod | Código de motivo de rechazo FCE |
| 14 | `FCE_RjRsnDes` | Edm.String | Yes | FCE Rj Rsn Des | Descripción del motivo de rechazo FCE |
| 15 | `GUID` | Edm.String | Yes | GUID | GUID |
| 16 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |

## Used by (service operations)

- [`ElectronicCommunicationActionService_AFE_FceAction_GetByFceID`](../Servicios/ElectronicCommunicationActionService.md#electroniccommunicationactionservice_afe_fceaction_getbyfceid)
