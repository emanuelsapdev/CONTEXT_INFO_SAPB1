# OTER - Territories

- **Tabla:** OTER
- **Descripción:** Territories
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTER.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `territryID` | Territory ID | Int | 11 | - |  |  |
| 2 | `descript` | Description | nVarChar | 200 | - |  |  |
| 3 | `parent` | Superordinate Object | Int | 11 | [OTER](OTER.md) | -1 |  |
| 4 | `lindex` | Location Index | Int | 11 | - |  |  |
| 5 | `inactive` | Inactive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | territryID |
| LOCATION | Yes | parent, lindex |
| DESCRIPT | No | descript |
