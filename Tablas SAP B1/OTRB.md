# OTRB - Tax Report Wizard for Brazil

- **Tabla:** OTRB
- **Descripción:** Tax Report Wizard for Brazil
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTRB.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `BPLId` | Branch ID | Int | 11 | [OBPL](OBPL.md) |  |  |
| 3 | `GPCId` | Government Payment Code | Int | 11 | [OGPC](OGPC.md) |  |  |
| 4 | `GPCCode` | Government Payment Code | nVarChar | 6 | - |  |  |
| 5 | `Year` | Reporting Year | Int | 6 | - |  |  |
| 6 | `PrdType` | Period Type | VarChar | 1 | - |  | `Q` = Quarter<br>`M` = Month<br>`H` = Half Month<br>`T` = Ten Days |
| 7 | `PrdNum` | Period Number | Int | 11 | - |  |  |
| 8 | `PrdDate` | Period Date To | Date | 8 | - |  |  |
| 9 | `RunName` | Wizard Run Name | nVarChar | 100 | - |  |  |
| 10 | `RunDate` | Wizard Run Date | Date | 8 | - |  |  |
| 11 | `Status` | Wizard Run Status | VarChar | 1 | - |  | `S` = Saved<br>`E` = Executed<br>`C` = Canceled |
| 12 | `StateTax` | State Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 14 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 15 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 16 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 17 | `CreateTime` | Generation Time | Int | 6 | - |  |  |
| 18 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SECONDARY | Yes | RunName |
