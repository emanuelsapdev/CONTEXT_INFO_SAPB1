# CHO2 - Checks for Payment - Print Status

- **Tabla:** CHO2
- **Descripción:** Checks for Payment - Print Status
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CHO2.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Index | Int | 11 | - |  |  |
| 2 | `ChkNum` | Check Number | Int | 11 | - |  |  |
| 3 | `Status` | Status | VarChar | 1 | - | N | `D` = Details<br>`V` = Void<br>`N` = Not Confirmed<br>`T` = Not Printed<br>`O` = Overflow |
| 4 | `PrnBy` | Printed By | Int | 6 | - |  |  |
| 5 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
