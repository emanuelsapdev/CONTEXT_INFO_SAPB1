# OUQR - Queries

- **Tabla:** OUQR
- **Descripción:** Queries
- **Cantidad de campos:** 28
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OUQR.html

## Campos (28)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IntrnalKey` | Internal Key | Int | 11 | - |  |  |
| 2 | `QCategory` | Query Category | Int | 11 | [OQCN](OQCN.md) |  |  |
| 3 | `QName` | Query Description | nVarChar | 100 | - |  |  |
| 4 | `QString` | Query | Text | 16 | - |  |  |
| 5 | `QType` | Query Type | VarChar | 1 | - | W | `R` = Regular<br>`W` = Wizard<br>`G` = Report Generator<br>`S` = Stored Procedure |
| 6 | `ColumnSize` | Column Size | nVarChar | 100 | - |  |  |
| 7 | `DBType` | DB Type | Int | 11 | - |  |  |
| 8 | `QLastDate` | Last Upload Date | Date | 8 | - |  |  |
| 9 | `QLastTime` | Last Upload Time | Int | 6 | - |  |  |
| 10 | `Xslt` | XSLT Transformation | Text | 16 | - |  |  |
| 11 | `MenuItem` | Specify Menu Item | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `MenuCapt` | Menu Caption | nVarChar | 254 | - |  |  |
| 13 | `FatherMenu` | Parent Menu ID | Int | 11 | - |  |  |
| 14 | `MenuPos` | Menu Position | Int | 6 | - |  |  |
| 15 | `MenuUid` | Menu UID | nVarChar | 32 | - |  |  |
| 16 | `CommandID` | Menu Command ID | Int | 11 | - |  |  |
| 17 | `UpdateDate` | Last Update Date | Date | 8 | - |  |  |
| 18 | `LastUpdate` | Last Update Time | Int | 11 | - |  |  |
| 19 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 20 | `CreateDate` | Created On | Date | 8 | - |  |  |
| 21 | `ChangeDate` | Change Date | Date | 8 | - |  |  |
| 22 | `CreateTS` | Creatn Time - Incl. Secs | Int | 11 | - |  |  |
| 23 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 24 | `UserSign` | Created By | Int | 6 | - |  |  |
| 25 | `UserSign2` | Updated By | Int | 6 | - |  |  |
| 26 | `AnaActive` | Analytics Active | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 27 | `DisplTile` | Display UDQ as Tile | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 28 | `UseNmParam` | Include Parameters | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IntrnalKey, QCategory |
| QNAME_K | Yes | QName, QCategory |
