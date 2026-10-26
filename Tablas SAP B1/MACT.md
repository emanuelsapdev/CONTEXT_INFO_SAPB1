# MACT - MACT

- **Tabla:** MACT
- **Descripción:** MACT
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MACT.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `guid` | Unique Id | nVarChar | 36 | - |  |  |
| 2 | `fatherId` | MOBJ id | nVarChar | 36 | - |  |  |
| 3 | `lineNum` | Line Number | Int | 11 | - |  |  |
| 4 | `actName` | Action Name | nVarChar | 50 | - |  |  |
| 5 | `noteSid` | Action Name String Index | Int | 11 | - |  |  |
| 6 | `note` | Note | nVarChar | 254 | - |  |  |
| 7 | `actType` | Action Type | VarChar | 1 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | fatherId, lineNum |
| GUID | Yes | guid |
| ACTION | Yes | fatherId, actName |
