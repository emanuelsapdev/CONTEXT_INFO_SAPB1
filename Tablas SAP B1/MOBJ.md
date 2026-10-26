# MOBJ - MOBJ

- **Tabla:** MOBJ
- **Descripción:** MOBJ
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MOBJ.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `guid` | Guid | nVarChar | 36 | - |  |  |
| 2 | `fatherId` | Father Id | nVarChar | 36 | - |  |  |
| 3 | `tableName` | Table Name | nVarChar | 50 | - |  |  |
| 4 | `fatheObjId` | Father Object Id | nVarChar | 36 | - |  |  |
| 5 | `note` | Note | nVarChar | 254 | - |  |  |
| 6 | `popCol1` | Popup Column 1 | nVarChar | 36 | - |  |  |
| 7 | `objId` | Internal Object Id | Int | 11 | - |  |  |
| 8 | `objArrayId` | Internal Object Array Number | Int | 11 | - |  |  |
| 9 | `allowAdd` | Allow Create | VarChar | 1 | - |  |  |
| 10 | `allowUpd` | Allow Update | VarChar | 1 | - |  |  |
| 11 | `allowDel` | Allow Remove | VarChar | 1 | - |  |  |
| 12 | `noteSid` |  | Int | 11 | - |  |  |
| 13 | `modeList` | Listview Mode | VarChar | 1 | - |  |  |
| 14 | `modeGet` | Get by Key Mode | VarChar | 1 | - |  |  |
| 15 | `isSystem` | Is System Table | VarChar | 1 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | guid |
| TABLE_NAME | Yes | tableName |
| FA_OBJ_ID | No | fatheObjId |
