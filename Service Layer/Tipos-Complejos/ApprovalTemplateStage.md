# ApprovalTemplateStage — Etapas del modelo de autorización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ApprovalTemplateStage`
- **Descripción (ES):** Etapas del modelo de autorización
- **Description (EN):** Approval Template Stage

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `SortID` | Edm.Int32 | Yes | Sort ID | ID de orden |
| 2 | `ApprovalStageCode` | Edm.Int32 | Yes | Approval Stage Code | Código de etapa de autorización |
| 3 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |

## Used by (properties)

- [ApprovalTemplate](../Entidades/ApprovalTemplates.md).`ApprovalTemplateStages`
