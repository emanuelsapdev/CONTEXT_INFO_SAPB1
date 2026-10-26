# CUDV - User-Defined Values

- **Tabla:** CUDV
- **Descripción:** User-Defined Values
- **Cantidad de campos:** 22
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CUDV.html

## Campos (22)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FormID` | Form ID | nVarChar | 100 | - |  |  |
| 2 | `ItemID` | Field | nVarChar | 52 | - |  |  |
| 3 | `ColID` | Column ID | nVarChar | 128 | - | -1 |  |
| 4 | `ActionT` | Action | Int | 6 | - | 0 | `0`<br>`1` = Filtered List<br>`2` = Formula |
| 5 | `QueryId` | Query ID | Int | 11 | [OUQR](OUQR.md) |  |  |
| 6 | `IndexID` | Index | Int | 11 | - |  |  |
| 7 | `Refresh` | Refresh | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `FieldID` | Field | nVarChar | 60 | - |  |  |
| 9 | `FrceRfrsh` | Force Refresh | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `ByField` | By Field | VarChar | 1 | - | N | `Y` = When Field Changes<br>`N` = When Exiting Altered Column<br>`C` = When Column Value Changes |
| 11 | `ViewCmplt` | Allow to View Full List | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `ExpId` | Formula ID | Int | 11 | [CUVE](CUVE.md) |  |  |
| 13 | `BObject` | B Object | nVarChar | 254 | - |  |  |
| 14 | `DObject` | DB Object Name | nVarChar | 52 | - |  |  |
| 15 | `TrgType` | Auto Refresh Trigger Type | Int | 6 | - | 0 | `0` = Field Change<br>`1` = Event Happen<br>`2` = Field Change or Event Happen |
| 16 | `EvtTrg` | Event Trigger Value | Int | 11 | - |  |  |
| 17 | `CreateTS` | Create Time | Int | 11 | - |  |  |
| 18 | `UpdateTS` | Update Time | Int | 11 | - |  |  |
| 19 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 20 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 21 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 22 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IndexID |
| DETAILS | Yes | FormID, ItemID, ColID |
