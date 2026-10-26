# EVN2 - Event Notification Extended Data

- **Tabla:** EVN2
- **Descripción:** Event Notification Extended Data
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EVN2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `EventID` | Event ID | nVarChar | 50 | - |  |  |
| 2 | `WebhookID` | Webhook ID | nVarChar | 40 | - |  |  |
| 3 | `ExtData` | Extended Data | Text | 16 | - |  |  |
| 4 | `FilterExpV` | Value of Filter Expression | VarChar | 1 | - | 1 | `1` = True<br>`0` = False |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | EventID, WebhookID |
