# OEML - E-mail Log

- **Tabla:** OEML
- **Descripción:** E-mail Log
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OEML.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `CardName` | BP Name | nVarChar | 200 | - |  |  |
| 4 | `DocEntry` | Doc Internal Number | Int | 11 | - |  |  |
| 5 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 6 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 7 | `EMailAddr` | E-Mail Address | nVarChar | 100 | - |  |  |
| 8 | `SendDate` | Send Date | Date | 8 | - |  |  |
| 9 | `SendTime` | Time Sent | Int | 6 | - |  |  |
| 10 | `USERID` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `U_NAME` | User Name | nVarChar | 155 | - |  |  |
| 12 | `Subject` | Subject | nVarChar | 254 | - |  |  |
| 13 | `Body` | Body | Text | 16 | - |  |  |
| 14 | `AtcEntry` | Attachment Entry | Int | 11 | [OATC](OATC.md) |  |  |
| 15 | `AlertCode` | Alert Code | Int | 11 | [OALR](OALR.md) |  |  |
| 16 | `RecpntObjT` | Recipient Object Type | nVarChar | 20 | - |  |  |
| 17 | `RecpntObjC` | Recipient Object Code | nVarChar | 50 | - |  |  |
| 18 | `Confirmed` | E-Mail Sent Confirmation | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
