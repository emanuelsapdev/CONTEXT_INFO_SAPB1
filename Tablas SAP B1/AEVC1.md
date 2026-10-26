# AEVC1 - Event Subscription Details

- **Tabla:** AEVC1
- **Descripción:** Event Subscription Details
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AEVC1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WebhookID` | Webhook ID | nVarChar | 40 | - |  |  |
| 2 | `BizObject` | Business Object | nVarChar | 64 | - |  |  |
| 3 | `TransType` | Transaction Type | VarChar | 1 | - | A | `A` = Created<br>`U` = Updated<br>`D` = Deleted<br>`C` = Canceled<br>`O` = Reopened<br>`L` = Closed |
| 4 | `ObjectType` | Object Type | nVarChar | 30 | - |  |  |
| 5 | `LogInstanc` | Log instance | Int | 11 | - | 0 |  |
| 6 | `BOProps` | Business Object Properties | nVarChar | 254 | - |  |  |
| 7 | `FilterExpr` | Filter Expression | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WebhookID, BizObject, TransType, LogInstanc |
