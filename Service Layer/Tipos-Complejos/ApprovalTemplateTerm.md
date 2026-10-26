# ApprovalTemplateTerm — Condiciones del modelo de autorización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ApprovalTemplateTerm`
- **Descripción (ES):** Condiciones del modelo de autorización
- **Description (EN):** Approval Template Term

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ConditionType` | [ApprovalTemplateConditionTypeEnum](../Enums/ApprovalTemplateConditionTypeEnum.md) | Yes | Condition Type | Tipo de condición |
| 2 | `OperationType` | [ApprovalTemplateOperationTypeEnum](../Enums/ApprovalTemplateOperationTypeEnum.md) | Yes | Operation Type | Tipo de operación |
| 3 | `Value` | Edm.String | Yes | Value | Valor |

## Used by (properties)

- [ApprovalTemplate](../Entidades/ApprovalTemplates.md).`ApprovalTemplateTerms`
