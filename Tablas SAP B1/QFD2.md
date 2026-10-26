# QFD2 - UDQ Parameters

- **Tabla:** QFD2
- **Descripción:** UDQ Parameters
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/QFD2.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IntrnalKey` | Internal Key | Int | 11 | - |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ParamName` | Parameter Name | nVarChar | 80 | - |  |  |
| 4 | `ParamDesc` | Parameter Description | nVarChar | 100 | - |  |  |
| 5 | `StartIndex` | Start Index | nVarChar | 254 | - |  |  |
| 6 | `SqlType` | Parameter Type | Int | 6 | - |  |  |
| 7 | `SqlTypNm` | Parameter Type Name | nVarChar | 50 | - |  |  |
| 8 | `DbTypeId` | Database Type ID | VarChar | 1 | - |  |  |
| 9 | `DbSize` | Database Size | Int | 11 | - |  |  |
| 10 | `DftValue` | Default Value | nVarChar | 254 | - |  |  |
| 11 | `IsMulti` | Is Multiple | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `Mandatory` | Is Mandatory | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 13 | `EditType` | Edit Type | VarChar | 1 | - |  |  |
| 14 | `RTable` | Related Table | nVarChar | 100 | - |  |  |
| 15 | `RColumn` | Related Column | nVarChar | 100 | - |  |  |
| 16 | `ValidVal` | Valid Values | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IntrnalKey, ParamName |
