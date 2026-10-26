# AFEFceAPCheckECM2EntryParams — [Loc. AR] Parámetros de verificación de entrada ECM de FCE de compras

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AFEFceAPCheckECM2EntryParams`
- **Descripción (ES):** [Loc. AR] Parámetros de verificación de entrada ECM de FCE de compras
- **Description (EN):** AFE Fce AP Check ECM 2 Entry Parameters

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `assignedID` | Edm.String | Yes | Assigned ID | ID asignado |
| 2 | `docType` | Edm.Int32 | Yes | Doc Type | Tipo de documento |
| 3 | `poi` | Edm.String | Yes | Poi | Punto de emisión |
| 4 | `folio` | Edm.Int32 | Yes | Folio | Folio |

## Used by (service operations)

- [`ElectronicCommunicationActionService_AFE_FceAP_CheckECM2Entry`](../Servicios/ElectronicCommunicationActionService.md#electroniccommunicationactionservice_afe_fceap_checkecm2entry)
