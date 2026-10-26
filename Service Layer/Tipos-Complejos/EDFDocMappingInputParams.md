# EDFDocMappingInputParams — Parámetros de entrada de mapeo de documentos electrónicos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EDFDocMappingInputParams`
- **Descripción (ES):** Parámetros de entrada de mapeo de documentos electrónicos
- **Description (EN):** EDF Document Mapping Input Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | [ElectronicDocProtocolCodeStrEnum](../Enums/ElectronicDocProtocolCodeStrEnum.md) | Yes | Code | Código |
| 2 | `DocType` | Edm.String | Yes | Document Type | Tipo de documento (artículos/servicios) |

## Used by (service operations)

- [`ElectronicDocumentService_GetDocMappingList`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_getdocmappinglist)
