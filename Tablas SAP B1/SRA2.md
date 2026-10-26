# SRA2 - Scheduled Report Run Output

- **Tabla:** SRA2
- **Descripción:** Scheduled Report Run Output
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SRA2.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ActionCode` | Action Code | Int | 11 | - |  |  |
| 2 | `Date` | Date of Run | Date | 8 | - |  |  |
| 3 | `Time` | Time of Run | Int | 11 | - |  |  |
| 4 | `Status` | Status | VarChar | 1 | - | 0 | `S` = Successful<br>`E` = In progress<br>`F` = Failure<br>`T` = Results to Be Distributed<br>`0` = Schedule Inactive<br>`1` = Report Scheduled |
| 5 | `ReturnCode` | Return Code | Int | 11 | - |  |  |
| 6 | `ReturnStr` | Return String | nVarChar | 250 | - |  |  |
| 7 | `ResDag` | Result in DAG format | Text | 16 | - |  |  |
| 8 | `ResPdf` | Result in PDF format | Text | 16 | - |  |  |
| 9 | `ResHtml` | Result in HTML format | Text | 16 | - |  |  |
| 10 | `ResXml` | Result in XML format | Text | 16 | - |  |  |
| 11 | `Results` | Result Availability | nVarChar | 10 | - | NNNN |  |
| 12 | `ResLog` | Report Creation Log | Text | 16 | - |  |  |
| 13 | `ErrScreen` | Error Screenshot | Text | 16 | - |  |  |
| 14 | `EmailPfx` | Email Subject Prefix | nVarChar | 254 | - |  |  |
| 15 | `SenderName` | Sender Name | nVarChar | 100 | - |  |  |
| 16 | `SenderMail` | Sender Email | nVarChar | 100 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ActionCode, Date, Time |
| ACTIONCODE | No | ActionCode |
