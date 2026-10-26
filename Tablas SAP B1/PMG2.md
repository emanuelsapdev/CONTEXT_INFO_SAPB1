# PMG2 - Project Management - Stages - Open Issues

- **Tabla:** PMG2
- **Descripción:** Project Management - Stages - Open Issues
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PMG2.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [PMG1](PMG1.md) |  |  |
| 2 | `LineID` | Row No. | Int | 11 | - |  |  |
| 3 | `StageID` | Stage ID | Int | 11 | - |  |  |
| 4 | `AREA` | Area | Int | 11 | [PMC3](PMC3.md) |  |  |
| 5 | `PRIORITY` | Priority | Int | 11 | - |  |  |
| 6 | `REMARKS` | Remarks | Text | 16 | - |  |  |
| 7 | `CLOSED` | Closed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `SOLUTIONID` | Solution Code | Int | 11 | [OSLT](OSLT.md) |  |  |
| 9 | `SOLUTION` | Solution Description | nVarChar | 254 | - |  |  |
| 10 | `RESPNSIBLE` | Responsible | Int | 11 | [OHEM](OHEM.md) |  |  |
| 11 | `ENTERED` | Entered By | Int | 11 | [OHEM](OHEM.md) |  |  |
| 12 | `DATE` | Date Entered | Date | 8 | - |  |  |
| 13 | `EFFORT` | Effort Costs | Num | 19.6 | - |  |  |
| 14 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 15 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineID |
