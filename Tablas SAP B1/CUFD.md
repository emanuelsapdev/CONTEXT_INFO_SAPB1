# CUFD - User Fields - Description

- **Tabla:** CUFD
- **Descripción:** User Fields - Description
- **Cantidad de campos:** 21
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CUFD.html

## Campos (21)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TableID` | Table | nVarChar | 21 | - |  |  |
| 2 | `FieldID` | Field | Int | 6 | - |  |  |
| 3 | `AliasID` | Title | nVarChar | 50 | - |  |  |
| 4 | `Descr` | Description | nVarChar | 80 | - |  |  |
| 5 | `TypeID` | Type | VarChar | 1 | - |  |  |
| 6 | `EditType` | Edit Type | VarChar | 1 | - |  |  |
| 7 | `SizeID` | Size | Int | 6 | - |  |  |
| 8 | `EditSize` | Edit Size | Int | 6 | - |  |  |
| 9 | `Dflt` | Default | nVarChar | 254 | - |  |  |
| 10 | `NotNull` | Required Entry Field | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `IndexID` | Create Index | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `RTable` | Linked Table | nVarChar | 21 | [OUTB](OUTB.md) |  |  |
| 13 | `RField` | Linked Field | Int | 6 | - |  |  |
| 14 | `Action` | Action | VarChar | 1 | - |  |  |
| 15 | `Sys` | System Defined? | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `DfltDate` | Default Date | Date | 8 | - |  |  |
| 17 | `RelUDO` | Related UDO | nVarChar | 20 | - |  |  |
| 18 | `ValidRule` | Validation Rule | nVarChar | 254 | - |  |  |
| 19 | `RelSO` | Related System Object | nVarChar | 20 | - |  |  |
| 20 | `RThrdPTab` | Related to Third Party Table | nVarChar | 100 | - |  |  |
| 21 | `RThrdPFld` | Related to Third Party Field | nVarChar | 100 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TableID, FieldID |
| ALIAS | Yes | TableID, AliasID |
