# AHE4 - Previous Employment

- **Tabla:** AHE4
- **Descripción:** Previous Employment
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AHE4.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `empID` | Employee No. | Int | 11 | [OHEM](OHEM.md) |  |  |
| 2 | `line` | Previous Employment Row | Int | 6 | - |  |  |
| 3 | `fromDate` | Employment from | Date | 8 | - |  |  |
| 4 | `toDate` | Employment to | Date | 8 | - |  |  |
| 5 | `employer` | Employer | nVarChar | 50 | - |  |  |
| 6 | `position` | Position | nVarChar | 50 | - |  |  |
| 7 | `remarks` | Previous Employment | Text | 16 | - |  |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 9 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | empID, line, LogInstanc |
