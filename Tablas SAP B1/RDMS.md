# RDMS - Dictionary Master

- **Tabla:** RDMS
- **Descripción:** Dictionary Master
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RDMS.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Num` | String number | Int | 11 | - |  |  |
| 2 | `Internal` | Internal | VarChar | 1 | - | 0 | `1` = Yes<br>`0` = No |
| 3 | `Created` | Creation date | Date | 8 | - |  |  |
| 4 | `Remarks` | Remarks | nVarChar | 250 | - |  |  |
| 5 | `SBOCode` | SBO Code | nVarChar | 30 | - |  |  |
| 6 | `StringType` | String Type | nVarChar | 4 | - |  |  |
| 7 | `MaxLen` | Maximum Length | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Num |
| SBO_CODE | Yes | SBOCode |
