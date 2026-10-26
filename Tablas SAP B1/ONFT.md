# ONFT - Nota Fiscal Tax Category (Brazil)

- **Tabla:** ONFT
- **Descripción:** Nota Fiscal Tax Category (Brazil)
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ONFT.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Tax Category | nVarChar | 20 | - |  |  |
| 3 | `Locked` | Locked | VarChar | 1 | - | N | `N`<br>`Y` |
| 4 | `GPCId` | Government Payment Code | Int | 11 | [OGPC](OGPC.md) | -1 |  |
| 5 | `CESTrel` | CEST Relevant | VarChar | 1 | - | N | `Y`<br>`N` |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| CODE | Yes | Code |
