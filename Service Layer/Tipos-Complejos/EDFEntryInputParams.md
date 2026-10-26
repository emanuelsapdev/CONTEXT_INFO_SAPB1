# EDFEntryInputParams — Parámetros de entrada de documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EDFEntryInputParams`
- **Descripción (ES):** Parámetros de entrada de documento electrónico
- **Description (EN):** EDF Entry Input Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | [ElectronicDocProtocolCodeStrEnum](../Enums/ElectronicDocProtocolCodeStrEnum.md) | Yes | Code | Código |
| 2 | `GUID` | Edm.String | Yes | GUID | GUID |

## Used by (service operations)

- [`ElectronicDocumentService_GetEntry`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_getentry)
