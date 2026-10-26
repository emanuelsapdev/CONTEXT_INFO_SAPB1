# TeamMember — Miembros del equipo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TeamMember`
- **Descripción (ES):** Miembros del equipo
- **Description (EN):** Team Member
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TeamID` | Edm.Int32 | Yes | Team ID | ID de equipo |
| 2 | `EmployeeID` | Edm.Int32 | Yes | Employee ID | ID de empleado |
| 3 | `RoleInTeam` | [BoRoleInTeam](../Enums/BoRoleInTeam.md) | Yes | Role In Team | Función en el equipo |

## Used by (properties)

- [Team](../Entidades/Teams.md).`TeamMembers`
