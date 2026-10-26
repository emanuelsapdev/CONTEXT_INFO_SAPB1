# ApprovalTemplateOperationTypeEnum — Operador de condición del modelo de autorización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ApprovalTemplateOperationTypeEnum`
- **Descripción (ES):** Operador de condición del modelo de autorización
- **Underlying type:** Edm.Int32
- **Members:** 9

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `opcodeUndefined` | 0 | Undefined | Indefinido |
| `opcodeGreaterThan` | 1 | Greater Than | Mayor que |
| `opcodeGreaterOrEqual` | 2 | Greater Or Equal | Mayor o igual que |
| `opcodeLessThan` | 3 | Less Than | Menor que |
| `opcodeLessOrEqual` | 4 | Less Or Equal | Menor o igual que |
| `opcodeEqual` | 5 | Equal | Igual a |
| `opcodeDoesNotEqual` | 6 | Does Not Equal | Distinto de |
| `opcodeInRange` | 7 | In Range | En el rango |
| `opcodeNotInRange` | 8 | Not In Range | Fuera del rango |

## Used by (1 properties)

- [ApprovalTemplateTerm](../Tipos-Complejos/ApprovalTemplateTerm.md).`OperationType`
