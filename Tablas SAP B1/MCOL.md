# MCOL - MCOL

- **Tabla:** MCOL
- **Descripción:** MCOL
- **Cantidad de campos:** 25
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MCOL.html

## Campos (25)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `guid` | Guid | nVarChar | 36 | - |  |  |
| 2 | `fatherId` | Object Id | nVarChar | 36 | - |  |  |
| 3 | `lineNum` | Line Number | Int | 11 | - |  |  |
| 4 | `colName` | Column Name | nVarChar | 50 | - |  |  |
| 5 | `colType` | Column Type | VarChar | 1 | - |  |  |
| 6 | `colSize` | Column Size | Int | 11 | - |  |  |
| 7 | `linkObjId` | Link to Object Id | nVarChar | 36 | - |  |  |
| 8 | `note` | Note | nVarChar | 254 | - |  |  |
| 9 | `defaultVal` | Default Value | nVarChar | 254 | - |  |  |
| 10 | `editSize` | Edit Size | Int | 11 | - |  |  |
| 11 | `mandatory` | Mandatory | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `editType` | Edit Type | VarChar | 1 | - |  |  |
| 13 | `rdOnlyAdd` | Read Only for Add Mode | VarChar | 1 | - |  |  |
| 14 | `rdOnlyUpd` | Read Only for Update Mode | VarChar | 1 | - |  |  |
| 15 | `supresZero` | Supress Zero | VarChar | 1 | - |  |  |
| 16 | `locale` | Localization | nVarChar | 254 | - |  |  |
| 17 | `onListEvt` | On List Event | VarChar | 1 | - |  |  |
| 18 | `onChgEvt` | On Change Event | VarChar | 1 | - |  |  |
| 19 | `noteSid` | String Id | Int | 11 | - |  |  |
| 20 | `width` | Width | Int | 11 | - |  |  |
| 21 | `noteList` | Listview Note | nVarChar | 254 | - |  |  |
| 22 | `noteLstSid` | String id of list view note | Int | 11 | - |  |  |
| 23 | `fieldType` | Field Type | Int | 11 | - |  |  |
| 24 | `diType` | DI API Fields | VarChar | 1 | - |  |  |
| 25 | `diBatType` | DI Batch Mode Type | VarChar | 1 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | fatherId, lineNum |
| GUID | Yes | guid |
| COL_NAME | No | fatherId, colName |
