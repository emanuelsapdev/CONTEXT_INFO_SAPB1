# SHQR - Upgrade queries history

- **Tabla:** SHQR
- **Descripción:** Upgrade queries history
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SHQR.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Version` | Version | Int | 11 | - |  |  |
| 2 | `TableId` | Metadata CAB | nVarChar | 4 | - |  |  |
| 3 | `Instance` | Query instance | Int | 6 | - |  |  |
| 4 | `DoBefore` | Do Before | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `QurString` | Query String | Text | 16 | - |  |  |
| 6 | `ServerType` | Server Type | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Version, TableId, Instance, DoBefore, ServerType |
