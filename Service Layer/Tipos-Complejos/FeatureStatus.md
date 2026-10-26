# FeatureStatus — Estado de funcionalidad

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `FeatureStatus`
- **Descripción (ES):** Estado de funcionalidad
- **Description (EN):** Feature Status

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FeatureID` | Edm.String | Yes | Feature ID | ID de funcionalidad |
| 2 | `Blocked` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Blocked | Bloqueado |

## Used by (service operations)

- [`CompanyService_GetFeaturesStatus`](../Servicios/CompanyService.md#companyservice_getfeaturesstatus)
