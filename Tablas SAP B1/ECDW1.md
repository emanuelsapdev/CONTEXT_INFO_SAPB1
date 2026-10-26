# ECDW1 - ECD Wizard - Rows 1

- **Tabla:** ECDW1
- **Descripción:** ECD Wizard - Rows 1
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ECDW1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocType` | Template Type | VarChar | 1 | - |  | `B` = Balance Sheet<br>`P` = Profit and Loss |
| 3 | `ExNumData1` | Extra Numeric Data 1 | Int | 11 | - |  |  |
| 4 | `ExNumData2` | Extra Numeric Data 2 | Int | 11 | - |  |  |
| 5 | `ExNumData3` | Extra Numeric Data 3 | Int | 11 | - |  |  |
| 6 | `ExStrData1` | Extra String Data 1 | nVarChar | 254 | - |  |  |
| 7 | `ExStrData2` | Extra String Data 2 | nVarChar | 254 | - |  |  |
| 8 | `ExStrData3` | Extra String Data 3 | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, DocType, ExNumData1, ExNumData2 |
