# ACPA1 - Periods Category - WIP Mapping - Log

- **Tabla:** ACPA1
- **Descripción:** Periods Category - WIP Mapping - Log
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACPA1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OACP](OACP.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 4 | `AcctFrom` | Consolidate from Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 5 | `AcctTo` | Consolidate to Account | nVarChar | 15 | [OACT](OACT.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum, LogInstanc |
