# ODMW - Data Migration

- **Tabla:** ODMW
- **Descripción:** Data Migration
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODMW.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Package Code | Int | 11 | - |  |  |
| 2 | `Name` | Package Name | nVarChar | 20 | - |  |  |
| 3 | `CategoryId` | Category ID | Int | 11 | [OQCN](OQCN.md) |  |  |
| 4 | `DestPath` | Dest. Path | Text | 16 | - |  |  |
| 5 | `Extantion` | Exported | nVarChar | 5 | - |  |  |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `Delim` | Include Title | nVarChar | 10 | - | T | `T` = Tab<br>`K` = ,<br>`D` = ;<br>`S` = Space |
| 8 | `InclTitle` | Set to Exported | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `SetExp` | New Records | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `NewRecs` | Save | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `Summary` | Summary | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
| NAME | Yes | Name |
