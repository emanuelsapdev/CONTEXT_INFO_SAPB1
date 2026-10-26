# OPHA - Project Management Subproject

- **Tabla:** OPHA
- **Descripción:** Project Management Subproject
- **Cantidad de campos:** 23
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPHA.html

## Campos (23)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `OWNER` | Owner | Int | 11 | [OHEM](OHEM.md) |  |  |
| 3 | `NAME` | Name | nVarChar | 254 | - |  |  |
| 4 | `START` | Subproject Start Date | Date | 8 | - |  |  |
| 5 | `FINISHED` | Deduction - Percentage | Num | 19.6 | - |  |  |
| 6 | `ParentID` | Parent Subproject | Int | 11 | - |  |  |
| 7 | `ProjectID` | Project No. | Int | 11 | [OPMG](OPMG.md) |  |  |
| 8 | `Code` | Subproject No. | Int | 11 | - |  |  |
| 9 | `TYP` | Subproject Type | Int | 11 | [PMC1](PMC1.md) |  |  |
| 10 | `CONTRIB` | Subproject Contribution - Percentage | Num | 19.6 | - |  |  |
| 11 | `STATUS` | Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 12 | `END` | Subproject End Date | Date | 8 | - |  |  |
| 13 | `COST` | Actual Cost | Num | 19.6 | - |  |  |
| 14 | `PLANNED` | Planned Cost | Num | 19.6 | - |  |  |
| 15 | `Level` | Depth of Subproject within the project | Int | 11 | - |  |  |
| 16 | `DUEDATE` | Due Date | Date | 8 | - |  |  |
| 17 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 18 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 19 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 20 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 21 | `CreateDate` | Production Date | Date | 8 | - |  |  |
| 22 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 23 | `BPLid` | Business Place ID | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
