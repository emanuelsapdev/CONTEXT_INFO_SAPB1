# ORCL - Recurring Transaction Instances

- **Tabla:** ORCL
- **Descripción:** Recurring Transaction Instances
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORCL.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `RcpEntry` | Template Entry | Int | 11 | [ORCP](ORCP.md) |  |  |
| 3 | `Instance` | Recurrence Instance | Int | 11 | - | 0 |  |
| 4 | `PlanDate` | Scheduled Date | Date | 8 | - |  |  |
| 5 | `Status` | Recurrence Status | VarChar | 1 | - | N | `N` = Not Executed<br>`E` = Executed<br>`R` = Removed |
| 6 | `DocObjType` | Document Object Type | nVarChar | 20 | - |  | `13` = Invoice<br>`112` = Draft |
| 7 | `DocEntry` | Created Doc Entry | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
