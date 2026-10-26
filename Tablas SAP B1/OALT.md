# OALT - Alerts Management

- **Tabla:** OALT
- **Descripción:** Alerts Management
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OALT.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Internal Number | Int | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 254 | - |  |  |
| 3 | `Type` | Type | VarChar | 1 | - | U | `S` = System Alert<br>`U` = User Alert |
| 4 | `Priority` | Priority | VarChar | 1 | - | 1 | `0` = Low<br>`1` = Normal<br>`2` = High |
| 5 | `Active` | Active Alert | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `NumOfParam` | No. of Parameters | Int | 11 | - |  |  |
| 7 | `ParamData` | Parameters | Text | 16 | - |  |  |
| 8 | `Params` | Parameters | Text | 16 | - |  |  |
| 9 | `NumOfDocs` | Documents Numbers | Int | 11 | - |  |  |
| 10 | `DocsData` | Documents | Text | 16 | - |  |  |
| 11 | `Docs` | Documents | Text | 16 | - |  |  |
| 12 | `UserText` | MEMO | Text | 16 | - |  |  |
| 13 | `QueryId` | Query | Int | 11 | - |  |  |
| 14 | `FrqncyType` | Frequency Type | VarChar | 1 | - | H | `S` = Minutes<br>`H` = Hours<br>`D` = Days<br>`W` = Weeks<br>`M` = Months |
| 15 | `FrqncyIntr` | Frequency | Int | 11 | - | 1 |  |
| 16 | `ExecDaY` | Day of Execution | Int | 6 | - | 1 |  |
| 17 | `ExecTime` | Execution Hour | Int | 11 | - | 800 |  |
| 18 | `LastDate` | Execution Date | Date | 8 | - |  |  |
| 19 | `LastTIME` | Execution Time | Int | 6 | - |  |  |
| 20 | `NextDate` | Next Date | Date | 8 | - |  |  |
| 21 | `NextTime` | Next Hour | Int | 6 | - |  |  |
| 22 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 23 | `History` | Save History | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 24 | `QCategory` | Query Category | Int | 11 | [OUQR](OUQR.md) |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
| ACTIVE | No | Active |
| NAME | No | Name |
