# DGP4 - Business Place List

- **Tabla:** DGP4
- **Descripción:** Business Place List
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DGP4.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [ODGP](ODGP.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `BPLId` | Business Place ID | Int | 11 | [OBPL](OBPL.md) |  |  |
| 4 | `BPLName` | Business Place Name | nVarChar | 200 | - |  |  |
| 5 | `Checked` | Checked | VarChar | 1 | - | Y | `Y`<br>`N` |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
