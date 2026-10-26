# QFD1 - Query Fields Definition

- **Tabla:** QFD1
- **Descripción:** Query Fields Definition
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/QFD1.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IntrnalKey` | Internal Key | Int | 11 | - |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `FieldName` | Field Name | nVarChar | 80 | - |  |  |
| 4 | `FieldDesc` | Field Description | nVarChar | 100 | - |  |  |
| 5 | `OrigTable` | Original Table | nVarChar | 100 | - |  |  |
| 6 | `OrigField` | Original Field | nVarChar | 50 | - |  |  |
| 7 | `EditType` | Edit Type | VarChar | 1 | - |  | `-` = None<br>`T` = Tax<br>`R` = Rate<br>`P` = Price<br>`S` = Sum<br>`N` = Unit<br>`Q` = Quantity<br>`%` = Percent<br>`M` = Measure |
| 8 | `StatType` | Statistical Type | VarChar | 1 | - | D | `D` = Dimension<br>`M` = Measure |
| 9 | `AggrType` | Aggregation Type | VarChar | 1 | - | N | `N` = None<br>`S` = Sum<br>`A` = Average<br>`C` = Count<br>`M` = Minimum<br>`X` = Maximum |
| 10 | `LinkTable` | Linked Table | nVarChar | 100 | - |  |  |
| 11 | `DeciPlace` | Decimal Places | Int | 6 | - | 2 | `0` = No Decimals<br>`1` = One Decimal<br>`2` = Two Decimals<br>`3` = Three Decimals<br>`4` = Four Decimals<br>`5` = Five Decimals<br>`6` = No Rounding<br>`7` = Amounts<br>`8` = Prices<br>`9` = Rates<br>`10` = Quantities<br>`11` = Units<br>`12` = Percent |
| 12 | `DbType` | Database Type | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IntrnalKey, LineNum |
