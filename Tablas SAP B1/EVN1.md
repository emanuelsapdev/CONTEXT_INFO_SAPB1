# EVN1 - Event Notification Details

- **Tabla:** EVN1
- **Descripción:** Event Notification Details
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EVN1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `EventID` | Event ID | nVarChar | 50 | - |  |  |
| 2 | `WebhookID` | Webhook ID | nVarChar | 40 | - |  |  |
| 3 | `Status` | Event Status | VarChar | 1 | - | D | `F` = Failed<br>`D` = Delivered |
| 4 | `Retry` | Retry Times | Int | 11 | - |  |  |
| 5 | `ReturnCode` | Error Code | Int | 11 | - |  |  |
| 6 | `LastSentDT` | Last Sent Date | Date | 8 | - |  |  |
| 7 | `LastSentTM` | Last Sent Timestamp | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | EventID, WebhookID |
