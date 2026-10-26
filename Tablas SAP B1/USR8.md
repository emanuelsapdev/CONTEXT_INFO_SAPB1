# USR8 - Point of Issue User Association

- **Tabla:** USR8
- **Descripción:** Point of Issue User Association
- **Cantidad de campos:** 2
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/USR8.html

## Campos (2)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UserId` | User ID | Int | 6 | [OUSR](OUSR.md) |  |  |
| 2 | `PTICode` | POI Code | nVarChar | 5 | [OPTI](OPTI.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UserId, PTICode |
