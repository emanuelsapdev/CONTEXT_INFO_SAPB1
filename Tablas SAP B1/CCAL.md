# CCAL - Chinese Chart of Account Level Definition

- **Tabla:** CCAL
- **Descripción:** Chinese Chart of Account Level Definition
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CCAL.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `lvlIAccLe` | Length First Level Accounts | Int | 6 | - | 4 | `4` |
| 2 | `accLvlSet` | Account Level Set | VarChar | 1 | - | N | `N`<br>`Y` |
| 3 | `balIndSet` | Balance Dir Indicator Set | VarChar | 1 | - | N | `N`<br>`Y` |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | lvlIAccLe |
