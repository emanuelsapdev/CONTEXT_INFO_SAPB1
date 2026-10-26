# CTNS - Transaction Notification Setting

- **Tabla:** CTNS
- **Descripción:** Transaction Notification Setting
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CTNS.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal No. | Int | 11 | - |  |  |
| 2 | `ObjectId` | Business Object ID | nVarChar | 30 | - |  |  |
| 3 | `EnableAsyN` | Enable async notification | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `EnableTn` | Transaction Notification | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `EnablePTn` | Post Transaction Notification | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| OBJECT_ID | Yes | ObjectId |
