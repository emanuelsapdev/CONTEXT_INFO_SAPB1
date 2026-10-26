# EmergencyNumber — Número de emergencia

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EmergencyNumber`
- **Descripción (ES):** Número de emergencia
- **Description (EN):** Emergency Number

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Number` | Edm.String | Yes | Number | Número |
| 3 | `Code` | Edm.String | Yes | Code | Código |
| 4 | `Status` | Edm.String | Yes | Status | Estado |

## Used by (service operations)

- [`ElectronicDocumentService_AddEmergencyNumber`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_addemergencynumber)
- [`ElectronicDocumentService_GetEmergencyNumbers`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_getemergencynumbers)
