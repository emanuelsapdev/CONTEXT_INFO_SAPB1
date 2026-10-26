# SRA3 - Scheduled Report Recipients

- **Tabla:** SRA3
- **Descripción:** Scheduled Report Recipients
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SRA3.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ActionCode` | Action Code | Int | 11 | [OSRA](OSRA.md) |  |  |
| 2 | `RecipCode` | Recipient Code | Int | 11 | - |  |  |
| 3 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 4 | `ObjCode` | Object Code | nVarChar | 50 | - |  |  |
| 5 | `Name` | Name | nVarChar | 155 | - |  |  |
| 6 | `SendInter` | Send Internally | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `SendEmail` | Send as E-Mail | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `SendSMS` | Send as SMS | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `Email` | E-Mail Address | nVarChar | 100 | - |  |  |
| 10 | `Number` | Telephone Number | nVarChar | 100 | - |  |  |
| 11 | `AttachDAG` | Attach DAG | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `AttachPDF` | Attach PDF | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `AttachHTML` | Attach HTML | VarChar | 1 | - | N |  |
| 14 | `AttachXML` | Attach XML | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `ShowResult` | Results Visible to User | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ActionCode, RecipCode |
| USER | No | Name |
