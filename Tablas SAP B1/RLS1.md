# RLS1 - Reference Links Sources Definition

- **Tabla:** RLS1
- **Descripción:** Reference Links Sources Definition
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RLS1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [ORLS](ORLS.md) |  |  |
| 2 | `LineID` | Line Id | Int | 11 | - |  |  |
| 3 | `SrcObjType` | Source Object Type | nVarChar | 20 | - |  |  |
| 4 | `SrcArr` | Source of Posting | Int | 6 | - |  |  |
| 5 | `SrcFld` | Source Field | nVarChar | 21 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineID |
| OBJARRFLD | Yes | SrcObjType, SrcArr, SrcFld |
