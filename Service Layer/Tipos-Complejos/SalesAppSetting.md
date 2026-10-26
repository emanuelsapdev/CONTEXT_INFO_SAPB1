# SalesAppSetting — Configuración de la app de ventas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SalesAppSetting`
- **Descripción (ES):** Configuración de la app de ventas
- **Description (EN):** Sales App Setting

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.Int32 | Yes | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `AdvancedDashBoard` | Edm.Int32 | Yes | Advanced Dash Board | Dashboard avanzado |
| 4 | `CustomerAdvancedDashBoard` | Edm.Int32 | Yes | Customer Advanced Dash Board | Dashboard avanzado de clientes |

## Used by (service operations)

- [`MobileAppService_GetSalesAppSetting`](../Servicios/MobileAppService.md#mobileappservice_getsalesappsetting)
- [`MobileAppService_UpdateSalesAppSetting`](../Servicios/MobileAppService.md#mobileappservice_updatesalesappsetting)
