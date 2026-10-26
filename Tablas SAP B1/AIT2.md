# AIT2 - Items - Multiple Preferred Vendors - History

- **Tabla:** AIT2
- **Descripción:** Items - Multiple Preferred Vendors - History
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AIT2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `VendorCode` | Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 4 | `ObjType` | Object | nVarChar | 20 | [ADP1](ADP1.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode, VendorCode, LogInstanc |
