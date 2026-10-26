# UMNU - UMNU

- **Tabla:** UMNU
- **Descripción:** UMNU
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UMNU.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `guid` | Guid | nVarChar | 36 | - |  |  |
| 2 | `fatherId` | Fathter Id | nVarChar | 36 | - |  |  |
| 3 | `lineNum` | Line Num | Int | 11 | - |  |  |
| 4 | `menuName` | Menu Name | nVarChar | 254 | - |  |  |
| 5 | `linkType` | Link Type | VarChar | 1 | - |  |  |
| 6 | `linkTo` | LinkTo | nVarChar | 36 | - |  |  |
| 7 | `icon` | Icon | Int | 11 | - |  |  |
| 8 | `locale` | Localization Flag | nVarChar | 254 | - |  |  |
| 9 | `mnuNameSid` | Menu String Id | Int | 11 | - |  |  |
| 10 | `linkChart` | Linked Chart Id | nVarChar | 36 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | guid |
| FATHER_ID | No | fatherId |
