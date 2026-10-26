# EWBTransporterParams — Parámetros de transportistas EWB

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EWBTransporterParams`
- **Descripción (ES):** Parámetros de transportistas EWB
- **Description (EN):** EWB Transporter Parameters

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `TransporterCode` | Edm.String | Yes | Transporter Code | Código del transportista |
| 3 | `TransporterName` | Edm.String | Yes | Transporter Name | Nombre del transportista |
| 4 | `TransporterID` | Edm.String | Yes | Transporter ID | ID del transportista |

## Used by (service operations)

- [`EWBTransporterService_GetEWBTransporterList`](../Servicios/EWBTransporterService.md#ewbtransporterservice_getewbtransporterlist)
