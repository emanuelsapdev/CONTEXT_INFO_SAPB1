# NNM3 - Documents Numbering -Belgium Series

- **Tabla:** NNM3
- **Descripción:** Documents Numbering -Belgium Series
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/NNM3.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectCode` | Document | nVarChar | 20 | [ONNM](ONNM.md) |  |  |
| 2 | `Series` | Series | Int | 11 | - | 0 |  |
| 3 | `DocSubType` | VAT Code for Tax Invoice Rpt | nVarChar | 2 | - | -- |  |
| 4 | `logInstanc` | Log Instance - History | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectCode, DocSubType, Series |
| SERIES | No | Series |
