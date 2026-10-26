# VTR1 - Tax Groups

- **Tabla:** VTR1
- **Descripción:** Tax Groups
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/VTR1.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Abs Entry (Numerator) | Int | 11 | - |  |  |
| 2 | `ObjectCode` | Object Code | nVarChar | 30 | - |  |  |
| 3 | `Sum` | Sum | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `DispOrder` | Display Order | Int | 11 | - |  |  |
| 5 | `ObjectType` | Object Type | VarChar | 1 | - |  |  |
| 6 | `Selected` | Selected Object | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 7 | `FromObject` | From Object | nVarChar | 20 | - |  |  |
| 8 | `ToObject` | To Object | nVarChar | 20 | - |  |  |
| 9 | `Adtnl_Key` | Additional Key | VarChar | 1 | - |  |  |
| 10 | `Amount` | Amount | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, ObjectCode, Adtnl_Key |
