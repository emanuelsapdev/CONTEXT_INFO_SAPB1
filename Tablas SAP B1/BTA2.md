# BTA2 - Brazil Tax Adujstment - Taxes Paid in Advance

- **Tabla:** BTA2
- **Descripción:** Brazil Tax Adujstment - Taxes Paid in Advance
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BTA2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OBTA](OBTA.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `TaxEntry` | Tax Entry | Int | 11 | [TAX1](TAX1.md) |  |  |
| 4 | `TaxLine` | Tax Line | Int | 11 | [TAX1](TAX1.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
| TAX | Yes | AbsEntry, TaxEntry, TaxLine |
