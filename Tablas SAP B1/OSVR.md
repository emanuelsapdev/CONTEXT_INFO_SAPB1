# OSVR - Saved Reconciliations

- **Tabla:** OSVR
- **Descripción:** Saved Reconciliations
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSVR.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `acctCode` | Account Code | nVarChar | 15 | - |  |  |
| 2 | `endBalanc` | Bank Statement Ending Balance | Num | 19.6 | - |  |  |
| 3 | `endDate` | Bank Statement Ending Date | Date | 8 | - |  |  |
| 4 | `statemntNo` | Bank Statement Number | Int | 11 | - |  |  |
| 5 | `userSign` | Creating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `createDate` | Creation Date | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | acctCode |
