# OSCT - Service Call Types

- **Tabla:** OSCT
- **Descripción:** Service Call Types
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSCT.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `callTypeID` | Call Type ID | Int | 6 | - |  |  |
| 2 | `Name` | Name | nVarChar | 20 | - |  |  |
| 3 | `Descriptio` | Description | Text | 16 | - |  |  |
| 4 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | callTypeID |
| NAME | Yes | Name |
