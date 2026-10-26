# DashboardPackagesService — Servicio de paquetes de dashboard

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `DashboardPackagesService`
- **Descripción (ES):** Servicio de paquetes de dashboard
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`DashboardPackagesService_ImportDashboardPackage`](#dashboardpackagesservice_importdashboardpackage) | action | [DashboardPackageParams](../Tipos-Complejos/DashboardPackageParams.md) | Import Dashboard Package | Importar paquete de dashboard |

## DashboardPackagesService_ImportDashboardPackage

- **Descripción (ES):** Importar paquete de dashboard
- **Request:** `POST /b1s/v2/DashboardPackagesService_ImportDashboardPackage`
- **Parameters:** `DashboardPackageImportParams` ([DashboardPackageImportParams](../Tipos-Complejos/DashboardPackageImportParams.md))
- **Returns:** [DashboardPackageParams](../Tipos-Complejos/DashboardPackageParams.md)

```json
{
  "DashboardPackageImportParams": {
    "PackageFilePath": "string",
    ...
  }
}
```

