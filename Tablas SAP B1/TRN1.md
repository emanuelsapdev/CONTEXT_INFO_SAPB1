# TRN1 - Subtable of OTRN

- **Tabla:** TRN1
- **Descripción:** Subtable of OTRN
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TRN1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TrnAbsEntr` | OTRN Abs Entry | Int | 11 | - |  |  |
| 2 | `LineNum` | Line Number of Table | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item Code | nVarChar | 254 | - |  |  |
| 4 | `ItemType` | Item Type | nVarChar | 8 | - |  |  |
| 5 | `SlimType` | Slim Type | nVarChar | 8 | - |  |  |
| 6 | `MaxLength` | Max. Length | Int | 11 | - |  |  |
| 7 | `SourceText` | Source Text | Text | 16 | - |  |  |
| 8 | `Memo` | Memo | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TrnAbsEntr, LineNum |
| UniqueIdx | Yes | TrnAbsEntr, ItemType, ItemCode, LineNum |
