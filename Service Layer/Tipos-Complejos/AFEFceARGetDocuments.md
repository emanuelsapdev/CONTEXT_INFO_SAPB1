# AFEFceARGetDocuments — [Loc. AR] Parámetros para obtener documentos FCE de ventas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AFEFceARGetDocuments`
- **Descripción (ES):** [Loc. AR] Parámetros para obtener documentos FCE de ventas
- **Description (EN):** AFE Fce AR Get Documents

- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 3 | `ObjType` | Edm.String | Yes | Obj Type | Tipo de objeto |
| 4 | `DocSubType` | Edm.String | Yes | Document Sub Type | Subtipo de documento |
| 5 | `EDocType` | Edm.String | Yes | E Document Type | Tipo de documento electrónico |
| 6 | `PTICode` | Edm.String | Yes | PTI Code | Código PTI |
| 7 | `Letter` | Edm.String | Yes | Letter | Carta |
| 8 | `FolNumFrom` | Edm.Int32 | Yes | Fol Number From | Folio desde |
| 9 | `GUID` | Edm.String | Yes | GUID | GUID |

## Used by (service operations)

- [`ElectronicCommunicationActionService_AFE_FceAR_GetDocuments`](../Servicios/ElectronicCommunicationActionService.md#electroniccommunicationactionservice_afe_fcear_getdocuments)
