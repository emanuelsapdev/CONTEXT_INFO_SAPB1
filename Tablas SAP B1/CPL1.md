# CPL1 - Quick Copy - Instance Log

- **Tabla:** CPL1
- **Descripción:** Quick Copy - Instance Log
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CPL1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Document Number | Int | 11 | [OCPL](OCPL.md) |  |  |
| 2 | `LogId` | Log ID | Int | 11 | - |  |  |
| 3 | `ObjectID` | Object ID | nVarChar | 20 | - |  |  |
| 4 | `Instance` | Instance Key | nVarChar | 254 | - |  |  |
| 5 | `ErrCode` | Error Code | nVarChar | 20 | - |  |  |
| 6 | `MessageId` | Message ID | nVarChar | 20 | - |  |  |
| 7 | `MessageDes` | Message Description | nVarChar | 254 | - |  |  |
| 8 | `InstName` | Instance Name | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogId |
