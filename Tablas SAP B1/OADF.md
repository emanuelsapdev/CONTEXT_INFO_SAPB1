# OADF - Address Formats

- **Tabla:** OADF
- **Descripción:** Address Formats
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OADF.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | Int | 6 | - |  |  |
| 2 | `Name` | Name | nVarChar | 50 | - |  |  |
| 3 | `Format` | Format | nVarChar | 100 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `SuppBkLine` | Suppress Blank Lines | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
| ADF_NAME | Yes | Name |
