# WTQ7 - Inventory Transfer Request - Delivery Packages

- **Tabla:** WTQ7
- **Descripción:** Inventory Transfer Request - Delivery Packages
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WTQ7.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Document ID | Int | 11 | [OWTQ](OWTQ.md) |  |  |
| 2 | `PackageNum` | Package Number | Int | 11 | - |  |  |
| 3 | `PackageTyp` | Package Type | nVarChar | 30 | - |  |  |
| 4 | `Weight` | Weight | Num | 19.6 | - |  |  |
| 5 | `WeightUnit` | UoM | Int | 6 | [OWGT](OWGT.md) |  |  |
| 6 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 1250000001 |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 8 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, PackageNum |
