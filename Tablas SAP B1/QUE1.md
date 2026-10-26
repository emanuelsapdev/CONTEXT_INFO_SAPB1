# QUE1 - Queue Members

- **Tabla:** QUE1
- **Descripción:** Queue Members
- **Cantidad de campos:** 2
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/QUE1.html

## Campos (2)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `queueID` | Queue ID | nVarChar | 20 | [OQUE](OQUE.md) |  |  |
| 2 | `member` | Member Name | Int | 11 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | queueID, member |
