# ARSC1 - Resources - Warehouses - Log

- **Tabla:** ARSC1
- **Descripción:** Resources - Warehouses - Log
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ARSC1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ResCode` | Internal Resource ID | nVarChar | 50 | [ORSC](ORSC.md) |  |  |
| 2 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 3 | `Locked` | Locked | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 4 | `ObjType` | Object | nVarChar | 20 | - | 290 |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ResCode, WhsCode, LogInstanc |
| WHS | No | WhsCode |
