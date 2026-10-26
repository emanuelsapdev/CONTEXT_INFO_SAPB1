# HEM6 - Employee Roles

- **Tabla:** HEM6
- **Descripción:** Employee Roles
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/HEM6.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `empID` | Employee No. | Int | 11 | [OHEM](OHEM.md) |  |  |
| 2 | `line` | Employee Role Row | Int | 6 | - |  |  |
| 3 | `roleID` | Role ID | Int | 11 | [OHTY](OHTY.md) |  |  |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 5 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | empID, line |
