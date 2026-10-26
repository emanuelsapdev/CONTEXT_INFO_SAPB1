# BoApprovalRequestDecisionEnum — Decisión de la solicitud de autorización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoApprovalRequestDecisionEnum`
- **Descripción (ES):** Decisión de la solicitud de autorización
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ardPending` | 0 | Pending | Pendiente |
| `ardApproved` | 1 | Approved | Autorizado |
| `ardNotApproved` | 2 | Not Approved | No autorizado |

## Used by (2 properties)

- [ApprovalRequestDecision](../Tipos-Complejos/ApprovalRequestDecision.md).`Status`
- [ApprovalRequestLine](../Tipos-Complejos/ApprovalRequestLine.md).`Status`
