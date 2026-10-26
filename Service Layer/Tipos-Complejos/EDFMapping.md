# EDFMapping — Mapeo de documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EDFMapping`
- **Descripción (ES):** Mapeo de documento electrónico
- **Description (EN):** EDF Mapping

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FormatID` | Edm.Int32 | Yes | Format ID | ID de formato |
| 2 | `Hash` | Edm.String | Yes | Hash | Hash |
| 3 | `Name` | Edm.String | Yes | Name | Nombre |
| 4 | `Mapping` | Edm.String | Yes | Mapping | Mapeo |

## Used by (service operations)

- [`ElectronicDocumentService_GetMappingByHash`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_getmappingbyhash)
