# OCSQ - Column Sequences

- **Tabla:** OCSQ
- **Descripción:** Column Sequences
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCSQ.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Numerator | Int | 11 | - |  |  |
| 2 | `SeqType` | Sequence Type | nVarChar | 8 | - |  |  |
| 3 | `FormID` | Form ID | nVarChar | 20 | - |  |  |
| 4 | `ColToken` | Column Token | nVarChar | 20 | - |  |  |
| 5 | `VisualIndx` | Tabs Layout | Int | 11 | - |  |  |
| 6 | `VisInForm` | Visible in Form | VarChar | 1 | - | N | `Y`<br>`N` |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
