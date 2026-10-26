# SensitiveDataAccess — Acceso a datos sensibles

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SensitiveDataAccess`
- **Descripción (ES):** Acceso a datos sensibles
- **Description (EN):** Sensitive Data Access

- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Table` | Edm.String | Yes | Table | Tabla |
| 2 | `Key1` | Edm.String | Yes | Key 1 | Clave 1 |
| 3 | `Key2` | Edm.String | Yes | Key 2 | Clave 2 |
| 4 | `Key3` | Edm.String | Yes | Key 3 | Clave 3 |
| 5 | `Key4` | Edm.String | Yes | Key 4 | Clave 4 |
| 6 | `PropertyName` | Edm.String | Yes | Property Name | Nombre de propiedad |
| 7 | `PropertyID` | Edm.Int32 | Yes | Property ID | ID de propiedad |
| 8 | `PropertyValue` | Edm.String | Yes | Property Value | Valor de propiedad |

## Used by (service operations)

- [`SensitiveDataAccessService_Access`](../Servicios/SensitiveDataAccessService.md#sensitivedataaccessservice_access)
- [`SensitiveDataAccessService_IsDataSensitive`](../Servicios/SensitiveDataAccessService.md#sensitivedataaccessservice_isdatasensitive)
