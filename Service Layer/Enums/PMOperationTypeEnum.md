# PMOperationTypeEnum — Tipo de operación de gestión de proyectos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `PMOperationTypeEnum`
- **Descripción (ES):** Tipo de operación de gestión de proyectos
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `pm_op_Ignore` | 0 | Op Ignore | Ignorar |
| `pm_op_Add` | 1 | Op Add | Sumar |
| `pm_op_Subtract` | 2 | Op Subtract | Restar |

## Used by (2 properties)

- [PMS_DocumentData](../Tipos-Complejos/PMS_DocumentData.md).`Operation`
- [PM_DocumentData](../Tipos-Complejos/PM_DocumentData.md).`Operation`
