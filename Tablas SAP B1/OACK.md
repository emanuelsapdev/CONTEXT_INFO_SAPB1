# OACK - Acknowledge Number

- **Tabla:** OACK
- **Descripción:** Acknowledge Number
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OACK.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `FinYear` | Financial Year | Int | 11 | [OFYM](OFYM.md) |  |  |
| 3 | `Quarter` | Quarter | VarChar | 1 | - |  | `1` = Quarter 1<br>`2` = Quarter 2<br>`3` = Quarter 3<br>`4` = Quarter 4 |
| 4 | `AckNum` | Acknowledgment No. | nVarChar | 100 | - |  |  |
| 5 | `Location` | Location | Int | 11 | [OLCT](OLCT.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| LOC_QUART | Yes | FinYear, Quarter, Location |
