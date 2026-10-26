# PM_SubprojectParams — Gestión de proyectos - Parámetros de subproyecto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PM_SubprojectParams`
- **Descripción (ES):** Gestión de proyectos - Parámetros de subproyecto
- **Description (EN):** PM Subproject Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `IsSubproject` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Subproject | Es subproyecto |

## Used by (service operations)

- [`ProjectManagementService_GetSubprojectsList`](../Servicios/ProjectManagementService.md#projectmanagementservice_getsubprojectslist)
