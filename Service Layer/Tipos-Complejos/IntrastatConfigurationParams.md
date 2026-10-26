# IntrastatConfigurationParams — Parámetros de configuración de Intrastat

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `IntrastatConfigurationParams`
- **Descripción (ES):** Parámetros de configuración de Intrastat
- **Description (EN):** Intrastat Configuration Parameters

- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `ConfType` | [IntrastatConfigurationEnum](../Enums/IntrastatConfigurationEnum.md) | Yes | Conf Type | Tipo de configuración |
| 3 | `Code` | Edm.String | Yes | Code | Código |
| 4 | `StatCode` | Edm.String | Yes | Stat Code | Código estadístico |
| 5 | `DateFrom` | Edm.DateTimeOffset | Yes | Date From | Fecha desde |
| 6 | `DateTo` | Edm.DateTimeOffset | Yes | Date To | Fecha hasta |
| 7 | `Country` | Edm.String | Yes | Country | País |

## Used by (service operations)

- [`IntrastatConfigurationService_GetList`](../Servicios/IntrastatConfigurationService.md#intrastatconfigurationservice_getlist)
