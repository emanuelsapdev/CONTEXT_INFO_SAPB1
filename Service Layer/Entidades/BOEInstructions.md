# BOEInstructions — Instrucciones de letras de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BOEInstructions`
- **Descripción (ES):** Instrucciones de letras de cambio
- **Entity type:** `BOEInstruction`
- **Key:** `InstructionEntry` (Edm.Int32)
- **DB tables (main / lines):** [OIST](../../Tablas%20SAP%20B1/OIST.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BOEInstructions?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BOEInstructions/$count` | Contar |
| Get by key | `GET /b1s/v2/BOEInstructions(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BOEInstructions` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BOEInstructions(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BOEInstructions(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BOEInstructions(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `InstructionEntry` 🔑 | Edm.Int32 | No | Instruction Entry | Entrada de instrucción |
| 2 | `InstructionCode` | Edm.String | Yes | Instruction Code | Código de instrucción |
| 3 | `InstructionDesc` | Edm.String | Yes | Instruction Description | Descripción de la instrucción |
| 4 | `IsCancelInstruction` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Cancel Instruction | Es instrucción de cancelación |
