# OSTE - SAF-T Transaction Type

- **Tabla:** OSTE
- **Descripción:** SAF-T Transaction Type
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSTE.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 10 | - |  |  |
| 2 | `Desc` | Description | nVarChar | 200 | - |  |  |
| 3 | `DataSource` | Data Source | VarChar | 1 | - | N |  |
| 4 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 5 | `IsSys` | Is System | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
