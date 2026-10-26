# OPCI - Process Checklist Instance

- **Tabla:** OPCI
- **Descripción:** Process Checklist Instance
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPCI.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `InstancePk` | Instance Primary Key | Int | 11 | - |  |  |
| 2 | `TemplateFk` | Template Foreign Key | Int | 11 | [OPCT](OPCT.md) |  |  |
| 3 | `InstName` | Instance Name | nVarChar | 100 | - |  |  |
| 4 | `InstDesc` | Instance Description | nVarChar | 100 | - |  |  |
| 5 | `Creator` | Instance Creator | nVarChar | 100 | - |  |  |
| 6 | `Status` | Instance Status | VarChar | 1 | - | N | `N` = New<br>`P` = In Process<br>`F` = Finished |
| 7 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 8 | `CloseDate` | Close Date | Date | 8 | - |  |  |
| 9 | `CloPrcnt` | Closing Percentage | Num | 19.6 | - |  |  |
| 10 | `Memo` | Remarks | Text | 16 | - |  |  |
| 11 | `Attachment` | Attachment | Text | 16 | - |  |  |
| 12 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | InstancePk |
