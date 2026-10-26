# UDO4 - User-Defined Objects - Child Table Columns

- **Tabla:** UDO4
- **Descripción:** User-Defined Objects - Child Table Columns
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UDO4.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 20 | - |  |  |
| 2 | `ColumnNum` | Form Column Number | Int | 11 | - |  |  |
| 3 | `SonNum` | Child No. | Int | 11 | - |  |  |
| 4 | `ColAlias` | Form Column Alias | nVarChar | 52 | - |  |  |
| 5 | `ColDesc` | Form Column Description | nVarChar | 80 | - |  |  |
| 6 | `ColIsUsed` | Form Column Used or Not | VarChar | 1 | - | N |  |
| 7 | `ColEdit` | Form Column Actived or Not | VarChar | 1 | - | N |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, SonNum, ColumnNum |
