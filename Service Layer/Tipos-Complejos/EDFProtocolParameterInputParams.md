# EDFProtocolParameterInputParams — Parámetros de entrada de parámetro de protocolo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EDFProtocolParameterInputParams`
- **Descripción (ES):** Parámetros de entrada de parámetro de protocolo
- **Description (EN):** EDF Protocol Parameter Input Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | [ElectronicDocProtocolCodeStrEnum](../Enums/ElectronicDocProtocolCodeStrEnum.md) | Yes | Code | Código |
| 2 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `Branch` | Edm.Int32 | Yes | Branch | Sucursal |

## Used by (service operations)

- [`ElectronicDocumentService_GetProtocolParameter`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_getprotocolparameter)
