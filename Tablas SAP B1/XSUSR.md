# XSUSR - XApp User Authorization

- **Tabla:** XSUSR
- **Descripción:** XApp User Authorization
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/XSUSR.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `XID` | XID | nVarChar | 64 | - |  |  |
| 2 | `COMPANY` | COMPANY | nVarChar | 128 | - |  |  |
| 3 | `USER_CODE` | USER_CODE | nVarChar | 128 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | COMPANY, USER_CODE |
