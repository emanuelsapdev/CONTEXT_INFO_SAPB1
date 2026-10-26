# RUSR - Resource Users

- **Tabla:** RUSR
- **Descripción:** Resource Users
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RUSR.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IUserCode` | I User Code | nVarChar | 15 | - |  |  |
| 2 | `Name` | User Name | nVarChar | 30 | - |  |  |
| 3 | `UserGroup` | Authorization Group | Int | 11 | - |  |  |
| 4 | `Password` | Password | nVarChar | 20 | - |  |  |
| 5 | `UserSign` | User Signature | Int | 11 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UserSign |
| I_USER | Yes | IUserCode |
| NAME | Yes | Name |
