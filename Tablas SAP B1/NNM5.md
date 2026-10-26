# NNM5 - Document Numbering - Removed Serial Numbers

- **Tabla:** NNM5
- **Descripción:** Document Numbering - Removed Serial Numbers
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/NNM5.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectCode` | Document | nVarChar | 20 | - |  |  |
| 2 | `Series` | Series | Int | 11 | - |  |  |
| 3 | `DocSubType` | Document Subtype | nVarChar | 2 | - | -- |  |
| 4 | `Number` | Number | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Series, ObjectCode, DocSubType, Number |
| SERIES | No | Series, Number |
