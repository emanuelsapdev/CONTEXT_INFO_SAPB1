# PYD1 - Payment Terms Allowed in Payment Run

- **Tabla:** PYD1
- **Descripción:** Payment Terms Allowed in Payment Run
- **Cantidad de campos:** 2
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PYD1.html

## Campos (2)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PYDCode` | Payment Run Code | nVarChar | 20 | [OPYD](OPYD.md) |  |  |
| 2 | `PYMCode` | Payment Method | nVarChar | 15 | [OPYM](OPYM.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PYDCode, PYMCode |
