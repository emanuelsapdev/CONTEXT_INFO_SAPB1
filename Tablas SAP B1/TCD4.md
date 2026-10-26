# TCD4 - Withholding Tax Code Determination

- **Tabla:** TCD4
- **Descripción:** Withholding Tax Code Determination
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TCD4.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `Tcd2Id` | Determination Key Field ID | Int | 11 | - |  |  |
| 3 | `WTCode` | WTax Code | nVarChar | 8 | - |  |  |
| 4 | `Type` | WTax Code Type | VarChar | 1 | - | L | `R` = AR Default WT Code<br>`P` = AP Default WT Code<br>`L` = Line Item WT Code |
| 5 | `TcdId` | Tax Determination Code | Int | 11 | - |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
