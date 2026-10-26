# ARSC5 - Resources - Preferred Vendors - Log

- **Tabla:** ARSC5
- **Descripción:** Resources - Preferred Vendors - Log
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ARSC5.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ResCode` | Internal Resource ID | nVarChar | 50 | [ORSC](ORSC.md) |  |  |
| 2 | `VendorCode` | Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 4 | `ObjType` | Object | nVarChar | 20 | [ADP1](ADP1.md) | 290 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ResCode, VendorCode, LogInstanc |
