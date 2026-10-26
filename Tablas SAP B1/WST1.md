# WST1 - Confirmation Level - Rows

- **Tabla:** WST1
- **Descripción:** Confirmation Level - Rows
- **Cantidad de campos:** 2
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WST1.html

## Campos (2)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WstCode` | Code | Int | 11 | [OWST](OWST.md) |  |  |
| 2 | `UserID` | User Code | Int | 11 | [OUSR](OUSR.md) | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WstCode, UserID |
