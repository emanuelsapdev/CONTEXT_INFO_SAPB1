# QueueMember — Miembros de la cola

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `QueueMember`
- **Descripción (ES):** Miembros de la cola
- **Description (EN):** Queue Member
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `QueueID` | Edm.String | Yes | Queue ID | ID de cola |
| 2 | `MemberUserID` | Edm.Int32 | Yes | Member User ID | ID de usuario miembro |

## Used by (properties)

- [Queue](../Entidades/Queue.md).`QueueMembers`
