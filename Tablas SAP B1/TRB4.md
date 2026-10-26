# TRB4 - Tax Report Wizard - Selected Tax Entries

- **Tabla:** TRB4
- **Descripción:** Tax Report Wizard - Selected Tax Entries
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TRB4.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OTRB](OTRB.md) |  |  |
| 2 | `TaxSrcType` | Tax Source Object TYpe | Int | 11 | - | 10000011 | `10000011` = VAT Transactions<br>`243000003` = Brazil - Tax Adjustment |
| 3 | `TaxEntry` | Tax Entry | Int | 11 | - |  |  |
| 4 | `TaxLine` | Tax Line | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, TaxSrcType, TaxEntry, TaxLine |
