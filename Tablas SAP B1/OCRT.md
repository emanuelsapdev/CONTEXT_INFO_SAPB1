# OCRT - CRDB Tables Tree List

- **Tabla:** OCRT
- **Descripción:** CRDB Tables Tree List
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCRT.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ID` | ID | Int | 11 | - |  |  |
| 2 | `NodeStr` | Node String List | nVarChar | 20 | - |  |  |
| 3 | `FatherID` | Parent ID | Int | 11 | - |  |  |
| 4 | `TableName` | Table Name | nVarChar | 20 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
