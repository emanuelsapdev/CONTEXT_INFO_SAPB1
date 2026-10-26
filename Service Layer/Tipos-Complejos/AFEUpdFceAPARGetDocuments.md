# AFEUpdFceAPARGetDocuments — [Loc. AR] Actualización FCE de compras/ventas: documentos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AFEUpdFceAPARGetDocuments`
- **Descripción (ES):** [Loc. AR] Actualización FCE de compras/ventas: documentos
- **Description (EN):** AFE Upd Fce APAR Get Documents

- **Properties:** 13

## Properties (13)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `GUID` | Edm.String | Yes | GUID | GUID |
| 3 | `ActType` | Edm.Int32 | Yes | Act Type | Tipo de actividad |
| 4 | `ActStatus` | Edm.String | Yes | Act Status | Estado de actividad |
| 5 | `FCE_DcApStat` | Edm.String | Yes | FCE Dc Ap Stat | Estado de aceptación del documento FCE |
| 6 | `FCE_ApprStat` | Edm.String | Yes | FCE Appr Stat | Estado de aceptación FCE (Argentina) |
| 7 | `FCE_ID` | Edm.Int32 | Yes | FCE ID | ID FCE |
| 8 | `FCE_DocType` | Edm.Int32 | Yes | FCE Document Type | Tipo de documento FCE |
| 9 | `FCE_POI` | Edm.String | Yes | FCE POI | Punto de emisión FCE |
| 10 | `FCE_Folio` | Edm.Int32 | Yes | FCE Folio | Folio FCE |
| 11 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 12 | `UpdateTS` | Edm.Int32 | Yes | Update TS | Marca de tiempo de actualización |
| 13 | `isAP` | Edm.String | Yes | Is AP | Es de compras |

## Used by (service operations)

- [`ElectronicCommunicationActionService_AFE_UpdFceAPAR_GetDocuments`](../Servicios/ElectronicCommunicationActionService.md#electroniccommunicationactionservice_afe_updfceapar_getdocuments)
