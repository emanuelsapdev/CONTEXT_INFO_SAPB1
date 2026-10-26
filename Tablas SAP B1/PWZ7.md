# PWZ7 - Payment Wizard 7-Selected Branches

- **Tabla:** PWZ7
- **Descripción:** Payment Wizard 7-Selected Branches
- **Cantidad de campos:** 2
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PWZ7.html

## Campos (2)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IdNumber` | ID Number | Int | 11 | [OPWZ](OPWZ.md) |  |  |
| 2 | `BPLId` | Assigned Branch | Int | 11 | [OBPL](OBPL.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IdNumber, BPLId |
