# PQW3 - Purchase Quotation Generation Summary Report

- **Tabla:** PQW3
- **Descripción:** Purchase Quotation Generation Summary Report
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PQW3.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `JobID` | Job ID | Int | 11 | - |  |  |
| 2 | `SerialNum` | Serial Number | Int | 11 | - |  |  |
| 3 | `Severity` | Severity | VarChar | 1 | - |  |  |
| 4 | `MsgType` | Message Type | nVarChar | 50 | - |  |  |
| 5 | `MsgText` | Message Text | nVarChar | 200 | - |  |  |
| 6 | `MsgID` | Message ID | nVarChar | 100 | - |  |  |
| 7 | `Help` | Help | nVarChar | 100 | - |  |  |
| 8 | `Context` | Context | nVarChar | 100 | - |  |  |
| 9 | `DateTime` | Date and Time | nVarChar | 100 | - |  |  |
| 10 | `TrgDocType` | Target Document Type | Int | 11 | - |  |  |
| 11 | `TrgDocNum` | Target Document Number | Int | 11 | - |  |  |
| 12 | `TrgDocEnt` | Target Document Entry | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | JobID, SerialNum |
