# OCMF - Common Functions of Fiori-Style Cockpit

- **Tabla:** OCMF
- **Descripción:** Common Functions of Fiori-Style Cockpit
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCMF.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UserID` | User ID | Int | 6 | [OUSR](OUSR.md) |  |  |
| 2 | `ItemIndex` | Common Function Item Index | Int | 11 | - |  |  |
| 3 | `MenuUID` | Menu UID | nVarChar | 50 | - |  |  |
| 4 | `GroupID` | Authorization Group ID | Int | 6 | [OUGR](OUGR.md) |  |  |
| 5 | `MenuType` | Menu Type | VarChar | 1 | - | S | `S` = System Menu<br>`O` = Menu of User Defined Object<br>`Q` = Menu of User Defined Query<br>`A` = Menu added by UI API<br>`N` = Menu added by Unknown Source |
| 6 | `CmfMenuId` | Common Function Menu ID | nVarChar | 50 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UserID, ItemIndex |
| INDEX | No | ItemIndex |
