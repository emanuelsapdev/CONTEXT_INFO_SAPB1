# CSV17 - A/R Correction Invoice Reversal - Bin Allocation Data

- **Tabla:** CSV17
- **Descripción:** A/R Correction Invoice Reversal - Bin Allocation Data
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CSV17.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | [OCSV](OCSV.md) |  |  |
| 2 | `LineNum` | Bin Allocation Sequence | Int | 11 | - |  |  |
| 3 | `LogInstanc` | Line Number | Int | 11 | - | 0 |  |
| 4 | `ObjectType` | Subline Number | nVarChar | 20 | [ADP1](ADP1.md) | 166 |  |
| 5 | `ImpDocType` | SnB Type | VarChar | 1 | [OBSI](OBSI.md) |  |  |
| 6 | `ImpDocNum` | SnB Master Data Internal Number | nVarChar | 10 | - |  |  |
| 7 | `DateOfReg` | Bin Internal Number | Date | 8 | - |  |  |
| 8 | `CustClrDat` | Quantity | Date | 8 | - |  |  |
| 9 | `ConcActNum` | Item Code | nVarChar | 30 | - |  |  |
| 10 | `AdditNum` | Warehouse Code | nVarChar | 30 | - |  |  |
| 11 | `AddItmDV` | Object Type | Num | 19.6 | - |  |  |
| 12 | `tpVTransp` | Overland Transport Route | Int | 6 | - |  | `1` = Maritime<br>`2` = Waterway<br>`3` = Lakeside<br>`4` = Air<br>`5` = Post<br>`6` = Train<br>`7` = Road<br>`8` = Network Transmission<br>`9` = Own Means<br>`10` = Input/Output Fictitious<br>`11` = Courier<br>`12` = Hand Carry |
| 13 | `DrawSReg` | Drawback - Suspension Regime | nVarChar | 11 | - |  |  |
| 14 | `AddFrNavyA` | Additional Freight to Navy Authority | Num | 19.6 | - |  |  |
| 15 | `TypeOfImp` | Type of Import | VarChar | 1 | - |  |  |
| 16 | `nSeqAdic` | Additional Item Sequential Number | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
