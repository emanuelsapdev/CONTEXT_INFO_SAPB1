# OALR - Alerts

- **Tabla:** OALR
- **Descripción:** Alerts
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OALR.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Internal Number | Int | 11 | - |  |  |
| 2 | `Type` | Type | VarChar | 1 | - | A | `A` = Alert<br>`M` = Message |
| 3 | `Priority` | Priority | VarChar | 1 | - | 1 | `0` = -<br>`1`<br>`2` = mHighPriority |
| 4 | `TCode` | Template Code | Int | 11 | [OALT](OALT.md) |  |  |
| 5 | `Subject` | Subject | nVarChar | 254 | - |  |  |
| 6 | `UserText` | MEMO | Text | 16 | - |  |  |
| 7 | `DataCols` | No. of Columns | Int | 11 | - |  |  |
| 8 | `DataParams` | Data | Text | 16 | - |  |  |
| 9 | `MsgData` | Data | Text | 16 | - |  |  |
| 10 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `Attachment` | Attached File | Text | 16 | - |  |  |
| 12 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 13 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 14 | `AltType` | Alert Type | VarChar | 1 | - | N | `N` = Unknown<br>`C` = Inventory Cycle |
| 15 | `WddData` | Data of Approval Process | nVarChar | 254 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
| USER | No | UserSign |
