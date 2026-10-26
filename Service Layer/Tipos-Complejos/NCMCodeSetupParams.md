# NCMCodeSetupParams — Parámetros de configuración de códigos NCM

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `NCMCodeSetupParams`
- **Descripción (ES):** Parámetros de configuración de códigos NCM
- **Description (EN):** NCM Code Setup Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `NCMCode` | Edm.String | Yes | NCM Code | Código NCM |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |

## Used by (service operations)

- [`NCMCodesSetupService_GetNCMCodeSetupList`](../Servicios/NCMCodesSetupService.md#ncmcodessetupservice_getncmcodesetuplist)
