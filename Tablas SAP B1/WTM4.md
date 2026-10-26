# WTM4 - Approval Templates - Terms

- **Tabla:** WTM4
- **Descripción:** Approval Templates - Terms
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WTM4.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WtmCode` | Code | Int | 11 | [OWTM](OWTM.md) |  |  |
| 2 | `CondId` | Condition No. | Int | 11 | - | 0 | `1` = Deviation from Credit Limit<br>`2` = Deviation from Commitment<br>`3` = Gross Profit %<br>`4` = Discount %<br>`5` = Deviation from Budget<br>`7` = Quantity<br>`8` = Item Code<br>`9` = Total<br>`6` = Total Document<br>`10` = Counted Quantity<br>`11` = Variance<br>`12` = Variance %<br>`13` = Operating Profit %<br>`14` = Net Income %<br>`0` = Undefined Type |
| 3 | `opCode` | Ratio | Int | 6 | - | 0 | `1` = Greater Than<br>`2` = Greater or Equal<br>`3` = Less Than<br>`4` = Less or Equal<br>`5` = Equal<br>`6` = Does not Equal<br>`7` = In Range<br>`8` = Not in Range<br>`0` = Undefined Type |
| 4 | `opValue` | Value | nVarChar | 90 | - |  |  |
| 5 | `DecSep` | Decimal Separator | VarChar | 1 | - |  |  |
| 6 | `ThousSep` | Thousandths Separator | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WtmCode, CondId |
