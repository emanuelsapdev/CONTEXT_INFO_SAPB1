# SXROA - XLR Object Access

- **Tabla:** SXROA
- **Descripción:** XLR Object Access
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SXROA.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectAcce` | ObjectAccessId | Identity | 11 | - |  |  |
| 2 | `RoleId` | RoleId | nVarChar | 16 | - |  |  |
| 3 | `ObjId` | ObjId | nVarChar | 254 | - |  |  |
| 4 | `SubId` | SubId | nVarChar | 50 | - |  |  |
| 5 | `AccessLeve` | AccessLevel | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectAcce |
