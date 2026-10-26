# TRB3 - Tax Report Wizard - Selected Tax Categories

- **Tabla:** TRB3
- **Descripción:** Tax Report Wizard - Selected Tax Categories
- **Cantidad de campos:** 2
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TRB3.html

## Campos (2)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OTRB](OTRB.md) |  |  |
| 2 | `NfTaxId` | ID of Nota Fiscal Tax Category | Int | 11 | [ONFT](ONFT.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, NfTaxId |
