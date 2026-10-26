# AHTM - Employee Teams - Log

- **Tabla:** AHTM
- **Descripción:** Employee Teams - Log
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AHTM.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `teamID` | Team ID | Int | 11 | - |  |  |
| 2 | `name` | Team Name | nVarChar | 20 | - |  |  |
| 3 | `descriptio` | Description | Text | 16 | - |  |  |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | teamID, LogInstanc |
