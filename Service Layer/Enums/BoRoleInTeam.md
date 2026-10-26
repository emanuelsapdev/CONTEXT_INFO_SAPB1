# BoRoleInTeam — Función en el equipo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoRoleInTeam`
- **Descripción (ES):** Función en el equipo
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `borit_Leader` | 0 | Leader | Líder |
| `borit_Member` | 1 | Member | Miembro |

## Used by (1 properties)

- [TeamMember](../Tipos-Complejos/TeamMember.md).`RoleInTeam`
