# DMW1 - Query List

- **Tabla:** DMW1
- **Descripción:** Query List
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DMW1.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PacCode` | Package Code | Int | 11 | [ODMW](ODMW.md) |  |  |
| 2 | `QueryCode` | Query Code | Int | 11 | [OUQR](OUQR.md) |  |  |
| 3 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PacCode, QueryCode |
