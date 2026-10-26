# RLNG - ????

- **Tabla:** RLNG
- **Descripción:** ????
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RLNG.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Created` | Creation date | Date | 8 | - |  |  |
| 2 | `Updated` | Update date | Date | 8 | - |  |  |
| 3 | `Code` | Language code | Int | 11 | - |  |  |
| 4 | `Name` | Language name | nVarChar | 50 | - |  |  |
| 5 | `ShortName` | Short name | nVarChar | 4 | - |  |  |
| 6 | `Direction` | Direction | VarChar | 1 | - | 1 | `0` = Right to left<br>`1` = Left to right |
| 7 | `IsBase` | Is base | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 8 | `Charset` | Charset | Int | 11 | - |  |  |
| 9 | `CodePage` | Codepage | Int | 11 | - |  |  |
| 10 | `KBLayout` | Keyboard layout | Int | 11 | - |  |  |
| 11 | `LangStr` | Language String | nVarChar | 50 | - |  |  |
| 12 | `TransInB5I` | Translated In B5I System | VarChar | 1 | - | 0 |  |
| 13 | `HelpLang` | Online Help Language Code | nVarChar | 4 | - |  |  |
| 14 | `hasHotKey` | The language has hot key | VarChar | 1 | - | Y | `Y` = Has HotKey<br>`N` = Does not have HotKey |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
| BASE | No | IsBase |
| SHORT_NAME | Yes | ShortName |
