# ALT1 - Alerts - Users

- **Tabla:** ALT1
- **Descripción:** Alerts - Users
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ALT1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Internal Number | Int | 11 | - |  |  |
| 2 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 3 | `SendIntrnl` | Send Internally | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `SendEMail` | Send E-Mail | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `SendSMS` | Send SMS | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `SendFax` | Send Fax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, UserSign |
