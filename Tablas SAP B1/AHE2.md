# AHE2 - Education

- **Tabla:** AHE2
- **Descripción:** Education
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AHE2.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `empID` | Employee No. | Int | 11 | [OHEM](OHEM.md) |  |  |
| 2 | `line` | Education: Information Row | Int | 6 | - |  |  |
| 3 | `fromDate` | Education from | Date | 8 | - |  |  |
| 4 | `toDate` | Education to | Date | 8 | - |  |  |
| 5 | `type` | Education Type | Int | 11 | [OHED](OHED.md) |  |  |
| 6 | `institute` | Institute | nVarChar | 100 | - |  |  |
| 7 | `major` | Major | nVarChar | 50 | - |  |  |
| 8 | `diploma` | Diploma | nVarChar | 50 | - |  |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 10 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | empID, line, LogInstanc |
