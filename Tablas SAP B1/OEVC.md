# OEVC - Event Subscription

- **Tabla:** OEVC
- **Descripción:** Event Subscription
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OEVC.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WebhookID` | Webhook ID | nVarChar | 40 | - |  |  |
| 2 | `WebhookURL` | Webhook URL | nVarChar | 254 | - |  |  |
| 3 | `AuthType` | Authentication Type | VarChar | 1 | - | H | `N` = None<br>`B` = Basic<br>`O` = OAuth<br>`H` = HMAC<br>`S` = System |
| 4 | `AuthCred` | Authentication Credentials | Text | 16 | - |  |  |
| 5 | `Handshake` | Webhook Handshake | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 6 | `VerifyCert` | Verify Webhook Endpoint Certificate | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 7 | `State` | Webhook State | VarChar | 1 | - | A | `A` = Active<br>`I` = Inactive<br>`X` = Exceptional |
| 8 | `WorkMode` | Work Mode | VarChar | 1 | - | S | `S` = Standard<br>`R` = Replay |
| 9 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 10 | `CreateTime` | Creation Timestamp | Int | 11 | - |  |  |
| 11 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 12 | `UpdateTime` | Update Timestamp | Int | 11 | - |  |  |
| 13 | `LastSentDT` | Last Sent Date | Date | 8 | - |  |  |
| 14 | `LastSentTM` | Last Sent Timestamp | Int | 11 | - |  |  |
| 15 | `LastErrMsg` | Last Error Message | nVarChar | 254 | - |  |  |
| 16 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 17 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 18 | `DataVers` | Data Version | Int | 11 | - | 1 |  |
| 19 | `LogInstanc` | Log instance | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WebhookID |
| UNIQUE | Yes | WebhookURL |
