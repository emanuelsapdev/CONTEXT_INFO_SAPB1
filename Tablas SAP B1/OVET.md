# OVET - VAT Exemption Types

- **Tabla:** OVET
- **Descripción:** VAT Exemption Types
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OVET.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `typeID` | Type ID | Int | 6 | - |  |  |
| 2 | `TypeCode` | Type Code | nVarChar | 2 | - |  |  |
| 3 | `TypeName` | Type Name | nVarChar | 100 | - |  |  |
| 4 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | typeID |
