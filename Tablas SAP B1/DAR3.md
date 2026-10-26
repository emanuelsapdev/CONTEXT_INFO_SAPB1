# DAR3 - Data Archive - Handwritten Documents

- **Tabla:** DAR3
- **Descripción:** Data Archive - Handwritten Documents
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DAR3.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ArcEntry` | Data Archive Entry | Int | 11 | - |  |  |
| 2 | `Line_ID` | Row Number | Int | 11 | - |  |  |
| 3 | `DocType` | Document Type | nVarChar | 20 | - |  |  |
| 4 | `DocAbs` | Doc. No. | Int | 11 | - |  |  |
| 5 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 6 | `DocSubType` | Document Sub-Type | nVarChar | 2 | - | -- |  |
| 7 | `PIndicator` | Period Indicator | nVarChar | 10 | - | ' ' |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ArcEntry, Line_ID |
| DOC_NUM | No | DocType, DocSubType, DocNum, PIndicator |
