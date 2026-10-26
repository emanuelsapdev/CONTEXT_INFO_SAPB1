# DGP1 - Customer List

- **Tabla:** DGP1
- **Descripción:** Customer List
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DGP1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [ODGP](ODGP.md) |  |  |
| 2 | `CardCode` | Customer Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `CardName` | Customer Name | nVarChar | 200 | - |  |  |
| 4 | `Checked` | Checked | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `CtrlAcct` | Control Account | nVarChar | 15 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, CardCode |
