# OPSG - Product Source Code Groups

- **Tabla:** OPSG
- **Descripción:** Product Source Code Groups
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPSG.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `GroupCode` | Group No. | Int | 6 | - |  |  |
| 2 | `GroupName` | Group Name | nVarChar | 20 | - |  |  |
| 3 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | GroupCode |
| GROUP_NAME | Yes | GroupName |
