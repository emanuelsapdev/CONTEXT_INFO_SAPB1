# DADB - Data Archive DSA Balance

- **Tabla:** DADB
- **Descripción:** Data Archive DSA Balance
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DADB.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Document Internal ID | Int | 11 | - |  |  |
| 2 | `ItemCode` | Item Number | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 3 | `LocCode` | Location Code | Int | 11 | [OLCT](OLCT.md) |  |  |
| 4 | `OpenBal` | Opening Balance | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
