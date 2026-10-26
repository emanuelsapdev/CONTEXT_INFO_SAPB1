# OGFL - Grid Filter

- **Tabla:** OGFL
- **Descripción:** Grid Filter
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OGFL.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FormID` | Form ID | nVarChar | 20 | - |  |  |
| 2 | `GridID` | Grid ID | nVarChar | 11 | - |  |  |
| 3 | `UserCode` | User Code | Int | 6 | - |  |  |
| 4 | `DefFilter` | Default Filter | Int | 11 | - |  |  |
| 5 | `NextFltID` | Next Filter ID | Int | 11 | - | 1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | FormID, GridID, UserCode |
