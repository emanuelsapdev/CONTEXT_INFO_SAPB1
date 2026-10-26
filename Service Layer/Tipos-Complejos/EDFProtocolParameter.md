# EDFProtocolParameter — Parámetro de protocolo electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EDFProtocolParameter`
- **Descripción (ES):** Parámetro de protocolo electrónico
- **Description (EN):** EDF Protocol Parameter

- **Properties:** 15

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | [ElectronicDocProtocolCodeStrEnum](../Enums/ElectronicDocProtocolCodeStrEnum.md) | Yes | Code | Código |
| 2 | `ParamName` | Edm.String | Yes | Parameter Name | Nombre del parámetro |
| 3 | `ParamValue` | Edm.String | Yes | Parameter Value | Valor del parámetro |
| 4 | `ParameterID` | Edm.Int32 | Yes | Parameter ID | ID de parámetro |
| 5 | `BranchID` | Edm.Int32 | Yes | Branch ID | ID de sucursal |
| 6 | `ParamParameters` | Edm.String | Yes | Parameter Parameters | Parámetros del parámetro |
| 7 | `ParameterType` | Edm.String | Yes | Parameter Type | Tipo de parámetro |
| 8 | `Visible` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Visible | Visible |
| 9 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 10 | `CreateDate` | Edm.DateTimeOffset | Yes | Create Date | Fecha de creación |
| 11 | `UpdatingUser` | Edm.Int32 | Yes | Updating User | Usuario que actualiza |
| 12 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 13 | `LogInstance` | Edm.Int32 | Yes | Log Instance | Instancia de registro (historial) |
| 14 | `UIOrder` | Edm.Int32 | Yes | UI Order | Orden en la interfaz |
| 15 | `Type` | Edm.Int32 | Yes | Type | Tipo |

## Used by (properties)

- [EDFProtocolWithParameters](EDFProtocolWithParameters.md).`EDFProtocolParametersCollection`

## Used by (service operations)

- [`ElectronicDocumentService_GetProtocolParameter`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_getprotocolparameter)
- [`ElectronicDocumentService_UpdateProtocolParameter`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_updateprotocolparameter)
