# RGRP - users groups

- **Tabla:** RGRP
- **Descripción:** users groups
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RGRP.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `GroupCode` | Group Code | Int | 11 | - |  |  |
| 2 | `GroupName` | Group Name | nVarChar | 20 | - |  |  |
| 3 | `Perms` | Permissions | nVarChar | 250 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | GroupCode |
| NAME | Yes | GroupName |
