# OOCC - BoE Occurrence Code

- **Tabla:** OOCC
- **Descripción:** BoE Occurrence Code
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OOCC.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Code | nVarChar | 10 | - |  |  |
| 3 | `Dscription` | Description | nVarChar | 128 | - |  |  |
| 4 | `Note` | Note | nVarChar | 50 | - |  |  |
| 5 | `ReqBoeSt` | Requested BoE Status | VarChar | 1 | - |  | `G` = Generated<br>`S` = Sent<br>`D` = Deposited<br>`P` = Paid<br>`C` = Canceled<br>`F` = Failed |
| 6 | `IsMovement` | Is Movement | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE | Yes | Code, IsMovement |
