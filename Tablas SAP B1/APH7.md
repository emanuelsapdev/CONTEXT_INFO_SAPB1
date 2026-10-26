# APH7 - Project Management - Workorders - History

- **Tabla:** APH7
- **Descripción:** Project Management - Workorders - History
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/APH7.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [PHA1](PHA1.md) |  |  |
| 2 | `LineID` | Row No. | Int | 11 | - |  |  |
| 3 | `StageID` | Stage ID | Int | 11 | - |  |  |
| 4 | `DOCNUM` | Document Number | Int | 11 | - |  |  |
| 5 | `DocEntry` | Document Abs. Entry | Int | 11 | [OWOR](OWOR.md) |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 7 | `Chargeable` | Chargeable [Yes/No] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `Charged` | Charged | Num | 19.6 | - |  |  |
| 9 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineID, LogInstanc |
