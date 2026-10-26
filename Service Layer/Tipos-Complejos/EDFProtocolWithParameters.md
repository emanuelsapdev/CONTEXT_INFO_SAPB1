# EDFProtocolWithParameters — Protocolo electrónico con parámetros

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EDFProtocolWithParameters`
- **Descripción (ES):** Protocolo electrónico con parámetros
- **Description (EN):** EDF Protocol With Parameters

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | [ElectronicDocProtocolCodeStrEnum](../Enums/ElectronicDocProtocolCodeStrEnum.md) | Yes | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `IsActive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Active | Está activo |
| 4 | `EDFProtocolParametersCollection` | Collection([EDFProtocolParameter](../Tipos-Complejos/EDFProtocolParameter.md)) | Yes | EDF Protocol Parameters Collection | Colección de parámetros del protocolo electrónico |
| 5 | `PWPExtendedProperties` | [PWPExtendedProperties](../Tipos-Complejos/PWPExtendedProperties.md) | Yes | PWP Extended Properties | Propiedades ampliadas PWP |

## Used by (service operations)

- [`ElectronicDocumentService_UpdateExtendedProperties`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_updateextendedproperties)
