# RPRS - Print Sequence Definition

- **Tabla:** RPRS
- **Descripción:** Print Sequence Definition
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RPRS.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SeqID` | Sequence ID | Int | 11 | - |  |  |
| 2 | `SeqName` | Sequence Name | nVarChar | 254 | - |  |  |
| 3 | `LineNum` | Visual Order | Int | 6 | - |  |  |
| 4 | `ObjectID` | Document Object ID | Int | 11 | - |  |  |
| 5 | `SubDocType` | Document Subtype | Int | 6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SeqID |
| OBJECT_ID | No | ObjectID |
