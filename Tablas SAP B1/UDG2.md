# UDG2 - User Defaults - Credit Cards

- **Tabla:** UDG2
- **Descripción:** User Defaults - Credit Cards
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UDG2.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 8 | - |  |  |
| 2 | `CreditCard` | Credit Card Code | Int | 6 | [OCRC](OCRC.md) |  |  |
| 3 | `AcctCode` | Credit Amount Code | nVarChar | 15 | [OACT](OACT.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, CreditCard |
