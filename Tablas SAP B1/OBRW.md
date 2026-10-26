# OBRW - Browser Widget

- **Tabla:** OBRW
- **Descripción:** Browser Widget
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBRW.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Name` | Browser Widget Name | nVarChar | 100 | - |  |  |
| 3 | `Type` | Type | Int | 6 | - | 0 | `0` = Web Site<br>`1` = App |
| 4 | `Url` | Web Site or Extreme Application URL | nVarChar | 254 | - |  |  |
| 5 | `App` | Extreme Application Name | nVarChar | 100 | - |  |  |
| 6 | `Title` | Title | nVarChar | 254 | - |  |  |
| 7 | `ShowWebTil` | Display Web Page Title | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `Size` | Widget Size | nVarChar | 15 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| NAME | Yes | Name |
