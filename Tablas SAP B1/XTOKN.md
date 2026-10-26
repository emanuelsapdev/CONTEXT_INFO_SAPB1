# XTOKN - OIDC Offline Token

- **Tabla:** XTOKN
- **Descripción:** OIDC Offline Token
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/XTOKN.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UUID` | UUID | nVarChar | 40 | - |  |  |
| 2 | `UserCode` | User Code | nVarChar | 25 | - |  |  |
| 3 | `RefreToken` | Refresh Token | Text | 16 | - |  |  |
| 4 | `LastActive` | Last Active | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UUID |
