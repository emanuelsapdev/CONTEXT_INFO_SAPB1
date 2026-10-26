# OIST - BoE Instruction

- **Tabla:** OIST
- **Descripción:** BoE Instruction
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OIST.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `InstrCode` | Instruction | nVarChar | 2 | - |  |  |
| 3 | `InstrDespt` | Description | nVarChar | 128 | - |  |  |
| 4 | `IsCancel` | Is Cancellation | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE | Yes | InstrCode, IsCancel |
