# OWLPD - Launchpad

- **Tabla:** OWLPD
- **Descripción:** Launchpad
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWLPD.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Guid` | Guid | nVarChar | 40 | - |  |  |
| 2 | `UserId` | User Id | Int | 11 | - |  |  |
| 3 | `ThemeId` | Theme Id | nVarChar | 254 | - |  |  |
| 4 | `DisQikView` | Display Quick View or not | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `NtfShowDay` | Notification Show Days Setting | Int | 11 | - |  |  |
| 6 | `EnUsDfVl` | Enable User Define Value | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `UsDfVlDly` | User Defined Value Delay | Int | 11 | - |  |  |
| 8 | `WebSgtEb` | B1 WebClient Suggest: Enable | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 9 | `PrContLog` | Activity Reminder High Priority | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `PrRclFlag` | Execute Recurring Transactions Priority | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `PrdsplRate` | Exchange Rate Priority | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `HiPrBanEn` | High-Priority Banner Notification Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 13 | `PrAprvDsnc` | Approval Decision Notification Priority | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `PrReqAprvl` | Requests for Approval Notification Priority | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `PrRnwBlktA` | Renew Blanket Agreement Reminders Notification Priority | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `PrSvcClRem` | Service Call Reminders Notification Priority | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 17 | `PrSvcClAsn` | Service Call Assignments Notification Priority | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `PrWzdTsk` | Wizard Tasks Notification Priority | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 19 | `PrSvCnRnRm` | Service Contract Renewal Reminders Priority | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Guid |
