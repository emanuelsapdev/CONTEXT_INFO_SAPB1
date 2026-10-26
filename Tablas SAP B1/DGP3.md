# DGP3 - Expanded Consolidation Options

- **Tabla:** DGP3
- **Descripción:** Expanded Consolidation Options
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DGP3.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [ODGP](ODGP.md) |  |  |
| 2 | `CondNum` | Condition Number | Int | 11 | - |  |  |
| 3 | `ConFldID` | Consolidation Field ID | nVarChar | 100 | - |  |  |
| 4 | `Checked` | Checked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, CondNum |
