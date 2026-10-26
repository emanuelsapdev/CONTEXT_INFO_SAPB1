# OFIX - Fixed Asset Transactions

- **Tabla:** OFIX
- **Descripción:** Fixed Asset Transactions
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFIX.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `SrcObjType` | Source Object Type | nVarChar | 20 | - |  |  |
| 3 | `SrcObjAbs` | Source Object Internal ID | Int | 11 | - |  |  |
| 4 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `CancelDate` | Cancellation Date | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SECONDARY | No | SrcObjType, SrcObjAbs |
