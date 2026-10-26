# OBGD - Budget Cost Assess. Mthd

- **Tabla:** OBGD
- **Descripción:** Budget Cost Assess. Mthd
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBGD.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BgdCode` | Division Code | Int | 11 | - |  |  |
| 2 | `BgdName` | Description | nVarChar | 30 | - |  |  |
| 3 | `BgdTotal` | Budget Amount | Num | 19.6 | - |  |  |
| 4 | `Month1` | January | Num | 19.6 | - |  |  |
| 5 | `Month2` | February | Num | 19.6 | - |  |  |
| 6 | `Month3` | March | Num | 19.6 | - |  |  |
| 7 | `Month4` | April | Num | 19.6 | - |  |  |
| 8 | `Month5` | May | Num | 19.6 | - |  |  |
| 9 | `Month6` | June | Num | 19.6 | - |  |  |
| 10 | `Month7` | July | Num | 19.6 | - |  |  |
| 11 | `Month8` | August | Num | 19.6 | - |  |  |
| 12 | `Month9` | September | Num | 19.6 | - |  |  |
| 13 | `Month10` | October | Num | 19.6 | - |  |  |
| 14 | `Month11` | November | Num | 19.6 | - |  |  |
| 15 | `Month12` | December | Num | 19.6 | - |  |  |
| 16 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 17 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BgdCode |
| NAME | Yes | BgdName |
