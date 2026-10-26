# WMNU - WMNU

- **Tabla:** WMNU
- **Descripción:** WMNU
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WMNU.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjCode` | Object Code | Int | 11 | - |  |  |
| 2 | `ObjName` | Object Name | nVarChar | 20 | - |  |  |
| 3 | `FatherID` | Father Menu ID | Int | 11 | - |  |  |
| 4 | `BrothetID` | Older Brother Menu ID | Int | 11 | - |  |  |
| 5 | `KeyNum` | m_KeyNum | nVarChar | 100 | - |  |  |
| 6 | `ExCommand` | m_exCommand | nVarChar | 100 | - |  |  |
| 7 | `Params` | m_params | nVarChar | 100 | - |  |  |
| 8 | `ParamsEx` | m_paramsEx | nVarChar | 100 | - |  |  |
| 9 | `MatchFlag` | m_matchFlag | nVarChar | 100 | - |  |  |
| 10 | `Dag` | m_dag | nVarChar | 100 | - |  |  |
| 11 | `Form` | m_form | nVarChar | 100 | - |  |  |
| 12 | `RetProc` | m_paRetProc | nVarChar | 100 | - |  |  |
| 13 | `InitMode` | m_initialMode | nVarChar | 100 | - |  |  |
| 14 | `Message` | m_message | nVarChar | 100 | - |  |  |
| 15 | `KeyStr` | m_keyStr | nVarChar | 100 | - |  |  |
| 16 | `SubType` | m_subType | nVarChar | 100 | - |  |  |
| 17 | `Condition` | local setting condition | nVarChar | 254 | - |  |  |
| 18 | `FormProc` | Draw Form Proc | nVarChar | 100 | - |  |  |
| 19 | `StrList` | StrList Num | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjCode |
