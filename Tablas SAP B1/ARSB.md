# ARSB - Resource Groups - History

- **Tabla:** ARSB
- **Descripción:** Resource Groups - History
- **Cantidad de campos:** 32
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ARSB.html

## Campos (32)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ResGrpCod` | Number | Int | 6 | - |  |  |
| 2 | `ResGrpNam` | Group Name | nVarChar | 20 | - |  |  |
| 3 | `Locked` | Locked | VarChar | 1 | - | N | `N` = Changeable<br>`Y` = Locked |
| 4 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `Object` | Object Type - History | nVarChar | 20 | - | 292 |  |
| 7 | `logInstanc` | Log Instance - History | Int | 11 | - |  |  |
| 8 | `createDate` | Creation Date - History | Date | 8 | - |  |  |
| 9 | `userSign2` | Updating User - History | Int | 6 | - |  |  |
| 10 | `updateDate` | Date of Update - History | Date | 8 | - |  |  |
| 11 | `ResType` | Resource Type | VarChar | 1 | - | M | `M` = Machine<br>`L` = Labor<br>`O` = Other |
| 12 | `CostName1` | Resource Std Cost 1 | nVarChar | 254 | - |  |  |
| 13 | `CostVal1` | Resource Std Cost 1 | Num | 19.6 | - |  |  |
| 14 | `CostName2` | Resource Std Cost 2 | nVarChar | 254 | - |  |  |
| 15 | `CostVal2` | Resource Std Cost 2 | Num | 19.6 | - |  |  |
| 16 | `CostName3` | Resource Std Cost 3 | nVarChar | 254 | - |  |  |
| 17 | `CostVal3` | Resource Std Cost 3 | Num | 19.6 | - |  |  |
| 18 | `CostName4` | Resource Std Cost 4 | nVarChar | 254 | - |  |  |
| 19 | `CostVal4` | Resource Std Cost 4 | Num | 19.6 | - |  |  |
| 20 | `CostName5` | Resource Std Cost 5 | nVarChar | 254 | - |  |  |
| 21 | `CostVal5` | Resource Std Cost 5 | Num | 19.6 | - |  |  |
| 22 | `CostName6` | Resource Std Cost 2 | nVarChar | 254 | - |  |  |
| 23 | `CostVal6` | Resource Std Cost 6 | Num | 19.6 | - |  |  |
| 24 | `CostName7` | Resource Std Cost 7 | nVarChar | 254 | - |  |  |
| 25 | `CostVal7` | Resource Std Cost 7 | Num | 19.6 | - |  |  |
| 26 | `CostName8` | Resource Std Cost 8 | nVarChar | 254 | - |  |  |
| 27 | `CostVal8` | Resource Std Cost 8 | Num | 19.6 | - |  |  |
| 28 | `CostName9` | Resource Std Cost 9 | nVarChar | 254 | - |  |  |
| 29 | `CostVal9` | Resource Std Cost 9 | Num | 19.6 | - |  |  |
| 30 | `CostName10` | Resource Std Cost 10 | nVarChar | 254 | - |  |  |
| 31 | `CostVal10` | Resource Std Cost 10 | Num | 19.6 | - |  |  |
| 32 | `ResUoM` | Resource Unit of Measurement | nVarChar | 20 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ResGrpCod, logInstanc |
| GROUP_NAME | Yes | ResGrpNam, logInstanc |
