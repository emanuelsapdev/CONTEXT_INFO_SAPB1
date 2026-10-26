# CUMI - My Menu Items

- **Tabla:** CUMI
- **Descripción:** My Menu Items
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CUMI.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id_` | Folder Key | Int | 11 | - | 0 |  |
| 2 | `Name_` | Menu Item Name | nVarChar | 100 | - |  |  |
| 3 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 4 | `FatherId` | Parent Key | Int | 11 | - | -1 |  |
| 5 | `SortNum` | Sort Number | Int | 11 | - |  |  |
| 6 | `Type_` | Menu Item Type | VarChar | 1 | - | - | `F` = Form<br>`Q` = Query<br>`R` = Report<br>`L` = Link<br>`-` = Folder |
| 7 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) |  |  |
| 8 | `Key_` | Internal ID | nVarChar | 50 | - |  |  |
| 9 | `FormMenuId` | Form Menu ID | Int | 11 | - |  |  |
| 10 | `FormNum` | Form No. | Int | 11 | - |  |  |
| 11 | `RepPath` | Report Path | Text | 16 | - |  |  |
| 12 | `Levels` | Item Level | Int | 6 | - | 1 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UserSign, Id_ |
| DETAIL | No | UserSign, Name_, Levels, FatherId, SortNum |
