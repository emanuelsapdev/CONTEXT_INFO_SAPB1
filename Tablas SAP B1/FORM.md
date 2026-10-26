# FORM - FORM resource

- **Tabla:** FORM
- **Descripción:** FORM resource
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FORM.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Created` | Creation date | Date | 8 | - |  |  |
| 2 | `Updated` | Update date | Date | 8 | - |  |  |
| 3 | `Name` | Form name | nVarChar | 64 | - |  |  |
| 4 | `Num` | Form number | Int | 11 | - |  |  |
| 5 | `Type` | Form type | Int | 11 | - | 0 | `0` = Resize Document<br>`1` = Dialog Box<br>`3` = No Title Document<br>`4` = Fixed Document<br>`5` = Resize No Title Document<br>`6` = Toolbar<br>`7` = Fixed No Minimize |
| 6 | `CloseBox` | Close box | VarChar | 1 | - | 1 | `0` = No<br>`1` = Yes |
| 7 | `DfltButton` | Default button | Int | 11 | - | 0 |  |
| 8 | `_Top` | Top | Int | 11 | - |  |  |
| 9 | `_Bottom` | Bottom | Int | 11 | - |  |  |
| 10 | `_Left` | Left | Int | 11 | - |  |  |
| 11 | `_Right` | Right | Int | 11 | - |  |  |
| 12 | `MaxUnique` | Max Unique | Int | 11 | - |  |  |
| 13 | `RobjCode` | ImpExp Obj Code | Int | 11 | - | 0 |  |
| 14 | `HelpCntxt` | Help Context | nVarChar | 32 | - |  |  |
| 15 | `UsrSgnAttr` | User Sign For Attribs Change | Int | 11 | - | -1 |  |
| 16 | `ResCode` | Resource Code from RSBD | Int | 11 | - | -1 |  |
| 17 | `RevCode` | Revision Code | Int | 11 | - | -1 |  |
| 18 | `UseBoBind` | Use BO Binding | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Name, ResCode, RevCode |
| NUM | Yes | Num |
