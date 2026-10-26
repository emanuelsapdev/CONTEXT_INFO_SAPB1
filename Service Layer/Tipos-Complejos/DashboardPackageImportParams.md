# DashboardPackageImportParams — Parámetros de importación de paquete de dashboard

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DashboardPackageImportParams`
- **Descripción (ES):** Parámetros de importación de paquete de dashboard
- **Description (EN):** Dashboard Package Import Parameters

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PackageFilePath` | Edm.String | Yes | Package File Path | Ruta del archivo del paquete |
| 2 | `ImportQueries` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Import Queries | Consultas de importación |
| 3 | `ForceOverwriteQuery` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Force Overwrite Query | Forzar sobrescritura de la consulta |
| 4 | `ForceOverwritePackage` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Force Overwrite Package | Forzar sobrescritura del paquete |

## Used by (service operations)

- [`DashboardPackagesService_ImportDashboardPackage`](../Servicios/DashboardPackagesService.md#dashboardpackagesservice_importdashboardpackage)
