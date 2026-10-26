# DAL1 - Mapping between form item and dashboard column

- **Tabla:** DAL1
- **Descripción:** Mapping between form item and dashboard column
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DAL1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `LinkEntry` | Internal Key | Int | 11 | - |  |  |
| 3 | `ItemID` | Item ID | nVarChar | 250 | - |  |  |
| 4 | `ObjName` | Object Name | nVarChar | 250 | - |  |  |
| 5 | `PropName` | Property Name | nVarChar | 250 | - |  |  |
| 6 | `QueryCol` | Query Column | nVarChar | 250 | - |  |  |
| 7 | `MobDesc` | Mobile Description | nVarChar | 250 | - |  |  |
| 8 | `IsUDF` | Is UDF or Not | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
