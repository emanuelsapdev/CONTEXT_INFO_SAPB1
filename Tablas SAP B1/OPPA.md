# OPPA - Password Administration

- **Tabla:** OPPA
- **Descripción:** Password Administration
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPPA.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal ID | Int | 11 | - | 1 |  |
| 2 | `SecLevel` | Security Level | nVarChar | 20 | - | Low | `Low` = Low<br>`Medium` = Medium<br>`High` = High<br>`Custom` = Custom |
| 3 | `PwdExp` | Password Expiration | Int | 11 | - | 90 |  |
| 4 | `PwdMinLen` | Password Minimum Length | Int | 11 | - | 4 |  |
| 5 | `MinUppers` | Password Min. Uppercase Chars. | Int | 11 | - | 0 |  |
| 6 | `MinLowCase` | Password Min. Lowercase Chars. | Int | 11 | - | 0 |  |
| 7 | `MinDigits` | Password Minimum Digits | Int | 11 | - | 0 |  |
| 8 | `MinNonAlph` | Password Min. Non-alphanumeric Char. | Int | 11 | - | 0 |  |
| 9 | `NumPrevPwd` | Pwd does not match pwd rules | Int | 11 | - | 0 |  |
| 10 | `NumAuthLoc` | No. of Authentications Before Acct is Locked | Int | 11 | - | 100 |  |
| 11 | `PwdExample` | Password Example | nVarChar | 128 | - | abcd |  |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 13 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 14 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 15 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 16 | `UserSign2` | Updating User | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
