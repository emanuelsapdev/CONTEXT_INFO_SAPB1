# OPST - Service Call Problem Subtype

- **Tabla:** OPST
- **Descripción:** Service Call Problem Subtype
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPST.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ProSubTyId` | Problem Subtype ID | Int | 6 | - |  |  |
| 2 | `Name` | Name | nVarChar | 20 | - |  |  |
| 3 | `Descriptio` | Description | Text | 16 | - |  |  |
| 4 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ProSubTyId |
| NAME | Yes | Name |
