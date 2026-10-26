# AOB1 - Sent Messages - User History

- **Tabla:** AOB1
- **Descripción:** Sent Messages - User History
- **Cantidad de campos:** 25
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AOB1.html

## Campos (25)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AlertCode` | Alert Code | Int | 11 | [OALR](OALR.md) |  |  |
| 2 | `ObjType` | Object | nVarChar | 20 | - | 12 | `-1` = Random<br>`12` = User<br>`11` = Contact Person |
| 3 | `ObjCode` | Object Code | nVarChar | 50 | - |  |  |
| 4 | `ObjName` | Name | nVarChar | 155 | - |  |  |
| 5 | `SendIntrnl` | Sent Internally | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `Confirmed1` | Confirmation 1 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `ConfDate1` | Approval Time 1 | Date | 8 | - |  |  |
| 8 | `ConfTime1` | Approval Time 1 | Int | 6 | - |  |  |
| 9 | `SendEMail` | Sent E-mail | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `E_Mail` | E-Mail | nVarChar | 100 | - |  |  |
| 11 | `Info2` | Information 2 | Text | 16 | - |  |  |
| 12 | `Confirmed2` | Confirmation 2 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No<br>`E` = Error |
| 13 | `ConfDate2` | Authorization Period 2 | Date | 8 | - |  |  |
| 14 | `ConfTime2` | Authorization Period 2 | Int | 6 | - |  |  |
| 15 | `SendSMS` | Sent SMS | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `PortNum` | Mobile Phone Number | nVarChar | 50 | - |  |  |
| 17 | `Confirmed3` | Confirmation 3 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No<br>`E` = Error |
| 18 | `ConfDate3` | Approval Time 3 | Date | 8 | - |  |  |
| 19 | `ConfTime3` | Approval Time 3 | Int | 6 | - |  |  |
| 20 | `SendFax` | Sent Fax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `Fax` | Fax Number | nVarChar | 50 | - |  |  |
| 22 | `Confirmed4` | Confirmation 4 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No<br>`E` = Error |
| 23 | `ConfDate4` | Confirmation Date 4 | Date | 8 | - |  |  |
| 24 | `ConfTime4` | Confirmation Time 4 | Int | 6 | - |  |  |
| 25 | `SendAs` | Send As | VarChar | 1 | - | 0 | `0` = To<br>`1` = Cc<br>`2` = Bcc |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AlertCode, ObjType, ObjCode |
| SEND_EM | No | SendEMail |
| CONFIRMED2 | No | Confirmed2 |
