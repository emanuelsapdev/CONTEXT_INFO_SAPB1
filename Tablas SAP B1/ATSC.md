# ATSC - CST Code for Nota Fiscal

- **Tabla:** ATSC
- **Descripción:** CST Code for Nota Fiscal
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ATSC.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ID` | CST Internal Key | Int | 11 | - |  |  |
| 2 | `CODE` | CST Code Incoming | nVarChar | 20 | - |  |  |
| 3 | `Situation` | Description Incoming | Text | 16 | - |  |  |
| 4 | `Locked` | Locked | VarChar | 1 | - | N | `Y`<br>`N` |
| 5 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Incr.<br>`D` = Data Doc.<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `Category` | Tax Category | Int | 6 | [ONFT](ONFT.md) | -6 |  |
| 8 | `CodeOut` | CST Code Outgoing | nVarChar | 20 | - |  |  |
| 9 | `OutDesc` | Description Outgoing | Text | 16 | - |  |  |
| 10 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 11 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 12 | `UpdateDate` | Update Date | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID, LogInstanc |
| CST_CODE | Yes | CODE, Category, LogInstanc |
