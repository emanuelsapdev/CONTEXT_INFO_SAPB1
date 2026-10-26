# IGE9 - Goods Issue - Drawn Dpm

- **Tabla:** IGE9
- **Descripción:** Goods Issue - Drawn Dpm
- **Cantidad de campos:** 27
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IGE9.html

## Campos (27)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OIGE](OIGE.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `BaseAbs` | Base Document Internal ID | Int | 11 | - |  |  |
| 4 | `BaseLine` | Base Document Row | Int | 11 | - |  |  |
| 5 | `TargetBase` | Target or Base Document | VarChar | 1 | - | B | `B` = Base<br>`T` = Target |
| 6 | `ObjType` | Base Object Type | nVarChar | 20 | - |  |  |
| 7 | `DrawnSum` | Net LC | Num | 19.6 | - |  |  |
| 8 | `DrawnSumFc` | Net FC | Num | 19.6 | - |  |  |
| 9 | `DrawnSumSc` | Net SC | Num | 19.6 | - |  |  |
| 10 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 11 | `ObjCode` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 60 |  |
| 12 | `ApplDrawn` | Applied Net LC | Num | 19.6 | - |  |  |
| 13 | `ApplDrawnF` | Applied Net FC | Num | 19.6 | - |  |  |
| 14 | `ApplDrawnS` | Applied Net SC | Num | 19.6 | - |  |  |
| 15 | `BaseDocNum` | Base Document Number | Int | 11 | - |  |  |
| 16 | `BsDocDate` | Base Posting Date | Date | 8 | - |  |  |
| 17 | `BsDueDate` | Base Due Date | Date | 8 | - |  |  |
| 18 | `BsCardName` | Base BP Name | nVarChar | 200 | - |  |  |
| 19 | `BsComments` | Base Remarks | nVarChar | 254 | - |  |  |
| 20 | `Posted` | Base Document Posted | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 21 | `Vat` | Tax LC | Num | 19.6 | - |  |  |
| 22 | `VatFc` | Tax FC | Num | 19.6 | - |  |  |
| 23 | `VatSc` | Tax SC | Num | 19.6 | - |  |  |
| 24 | `Gross` | Gross LC | Num | 19.6 | - |  |  |
| 25 | `GrossFc` | Gross FC | Num | 19.6 | - |  |  |
| 26 | `GrossSc` | Gross SC | Num | 19.6 | - |  |  |
| 27 | `IsGross` | Is Gross Line | VarChar | 1 | - | N | `N` = Net Line<br>`Y` = Gross Line |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
