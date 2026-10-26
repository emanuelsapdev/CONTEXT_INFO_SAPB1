# WTM1 - Approval Templates - Producers

- **Tabla:** WTM1
- **Descripción:** Approval Templates - Producers
- **Cantidad de campos:** 2
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WTM1.html

## Campos (2)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WtmCode` | Code | Int | 11 | [OWTM](OWTM.md) |  |  |
| 2 | `UserID` | User Code | Int | 11 | [OUSR](OUSR.md) | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WtmCode, UserID |
