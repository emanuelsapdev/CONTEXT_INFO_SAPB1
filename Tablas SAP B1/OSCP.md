# OSCP - Service Call Problem Types

- **Tabla:** OSCP
- **Descripción:** Service Call Problem Types
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSCP.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `prblmTypID` | Problem Type ID | Int | 6 | - |  |  |
| 2 | `Name` | Name | nVarChar | 20 | - |  |  |
| 3 | `Descriptio` | Description | Text | 16 | - |  |  |
| 4 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | prblmTypID |
| NAME | Yes | Name |
