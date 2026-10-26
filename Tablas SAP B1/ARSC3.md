# ARSC3 - Resouces - Fixed Assets - Log

- **Tabla:** ARSC3
- **Descripción:** Resouces - Fixed Assets - Log
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ARSC3.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ResCode` | Internal Resource ID | nVarChar | 50 | [ORSC](ORSC.md) |  |  |
| 2 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ResCode, ItemCode, LogInstanc |
| ITEM_CODE | No | ItemCode |
