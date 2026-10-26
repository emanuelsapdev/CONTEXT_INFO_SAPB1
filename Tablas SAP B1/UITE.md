# UITE - UITE

- **Tabla:** UITE
- **Descripción:** UITE
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UITE.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `guid` | Guid | nVarChar | 36 | - |  |  |
| 2 | `fatherId` | Father Id | nVarChar | 36 | - |  |  |
| 3 | `itemOrder` | Item Order | Int | 11 | - |  |  |
| 4 | `itemLabel` | Item Label | nVarChar | 254 | - |  |  |
| 5 | `itemType` | Item Type | VarChar | 1 | - |  |  |
| 6 | `columnId` | Column Id | nVarChar | 36 | - |  |  |
| 7 | `sonFormId` | Son Form Id | nVarChar | 36 | - |  |  |
| 8 | `note` | Note | nVarChar | 254 | - |  |  |
| 9 | `groupId` | Group Id | nVarChar | 36 | - |  |  |
| 10 | `locale` | Localization Flag | nVarChar | 254 | - |  |  |
| 11 | `locVisible` | Visible Settings | nVarChar | 254 | - |  |  |
| 12 | `labelSid` | Item Name String Id | Int | 11 | - |  |  |
| 13 | `groupIcon` | Group Icon Index | Int | 11 | - |  |  |
| 14 | `groupType` | Group Type | VarChar | 1 | - |  |  |
| 15 | `actionId` |  | nVarChar | 36 | [MACT](MACT.md) |  |  |
| 16 | `linkButton` | Show Link Button | VarChar | 1 | - | N |  |
| 17 | `mVisible` | Mobile Visibility | VarChar | 1 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | fatherId, itemOrder |
| GUID | Yes | guid |
