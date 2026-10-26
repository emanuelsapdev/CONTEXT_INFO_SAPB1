# HEM3 - Employee Reviews

- **Tabla:** HEM3
- **Descripción:** Employee Reviews
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/HEM3.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `empID` | Employee No. | Int | 11 | [OHEM](OHEM.md) |  |  |
| 2 | `line` | Employee Review Row | Int | 6 | - |  |  |
| 3 | `date` | Employee Review Date | Date | 8 | - |  |  |
| 4 | `reviewDesc` | Review Description | nVarChar | 100 | - |  |  |
| 5 | `manager` | Manager | Int | 11 | [OHEM](OHEM.md) |  |  |
| 6 | `grade` | Grade | nVarChar | 50 | - |  |  |
| 7 | `remarks` | Reviews | Text | 16 | - |  |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 9 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | empID, line |
