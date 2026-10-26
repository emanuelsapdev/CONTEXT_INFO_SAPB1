# RPD17 - Goods Return - Import Process

- **Tabla:** RPD17
- **Descripción:** Goods Return - Import Process
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RPD17.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [ORPD](ORPD.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 4 | `ObjectType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 21 |  |
| 5 | `ImpDocType` | Type of Importation Document | VarChar | 1 | [OBSI](OBSI.md) |  |  |
| 6 | `ImpDocNum` | Importation Document Number | nVarChar | 10 | - |  |  |
| 7 | `DateOfReg` | Date of Registry DI/DSI/DA | Date | 8 | - |  |  |
| 8 | `CustClrDat` | Date of Customs Clearance | Date | 8 | - |  |  |
| 9 | `ConcActNum` | Drawback Concession Acct No. | nVarChar | 30 | - |  |  |
| 10 | `AdditNum` | Additional Number | nVarChar | 30 | - |  |  |
| 11 | `AddItmDV` | Additional Item Discount Value | Num | 19.6 | - |  |  |
| 12 | `tpVTransp` | Overland Transport Route | Int | 6 | - |  | `1` = Maritime<br>`2` = Waterway<br>`3` = Lakeside<br>`4` = Air<br>`5` = Post<br>`6` = Train<br>`7` = Road<br>`8` = Network Transmission<br>`9` = Own Means<br>`10` = Input/Output Fictitious<br>`11` = Courier<br>`12` = Hand Carry |
| 13 | `DrawSReg` | Drawback - Suspension Regime | nVarChar | 11 | - |  |  |
| 14 | `AddFrNavyA` | Additional Freight to Navy Authority | Num | 19.6 | - |  |  |
| 15 | `TypeOfImp` | Type of Import | VarChar | 1 | - |  |  |
| 16 | `nSeqAdic` | Additional Item Sequential Number | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
