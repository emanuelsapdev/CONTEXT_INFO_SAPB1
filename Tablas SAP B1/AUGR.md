# AUGR - Authorization Group - History

- **Tabla:** AUGR
- **Descripción:** Authorization Group - History
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AUGR.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `GroupId` | Authorization Group ID | Int | 6 | - |  |  |
| 2 | `GroupName` | Group Name | nVarChar | 155 | - |  |  |
| 3 | `GroupDec` | Group Description | nVarChar | 155 | - |  |  |
| 4 | `Allowences` | Allowances | Text | 16 | - |  |  |
| 5 | `TPLId` | Template ID | Int | 6 | [UICU](UICU.md) |  |  |
| 6 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 7 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 8 | `GroupType` | Group Type | VarChar | 1 | - | A | `A` = Authorization<br>`F` = Form Settings<br>`T` = Alerts<br>`U` = UI Configuration Templates<br>`L` = All |
| 9 | `CockpitId` | Cockpit Template ID | Int | 6 | - |  |  |
| 10 | `logInstanc` | Log Instance | Int | 11 | - |  |  |
| 11 | `userSign` | Creating User - History | Int | 6 | - |  |  |
| 12 | `createDate` | Creation Date - History | Date | 8 | - |  |  |
| 13 | `userSign2` | Updating User - History | Int | 6 | - |  |  |
| 14 | `updateDate` | Date of Update - History | Date | 8 | - |  |  |
| 15 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | GroupId, logInstanc |
| NAME_KEY | Yes | GroupName, logInstanc |
