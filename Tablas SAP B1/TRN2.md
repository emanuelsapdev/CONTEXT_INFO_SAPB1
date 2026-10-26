# TRN2 - Subtable of OTRN

- **Tabla:** TRN2
- **Descripción:** Subtable of OTRN
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TRN2.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TrnAbsEntr` | OTRN Abs Entry | Int | 11 | - |  |  |
| 2 | `LineNum` | Line Number of TRN1 | Int | 11 | - |  |  |
| 3 | `SubLineNum` | Subline Number | Int | 11 | - |  |  |
| 4 | `LangCode` | Language Code | Int | 11 | - |  |  |
| 5 | `Text` | Translated Text | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TrnAbsEntr, LineNum, SubLineNum |
| UniqueIdx | Yes | TrnAbsEntr, LineNum, LangCode |
