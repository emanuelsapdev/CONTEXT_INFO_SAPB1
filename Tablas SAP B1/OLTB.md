# OLTB - Location-based Tax Bal Table

- **Tabla:** OLTB
- **Descripción:** Location-based Tax Bal Table
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OLTB.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Numerator | Int | 11 | - |  |  |
| 2 | `LocCode` | Location Code | Int | 11 | [OLCT](OLCT.md) |  |  |
| 3 | `STAType` | Tax Type | Int | 11 | [OSTT](OSTT.md) |  |  |
| 4 | `STACode` | STA Code | nVarChar | 8 | [OSTA](OSTA.md) |  |  |
| 5 | `BalaType` | Balance Type | VarChar | 1 | - |  | `P`<br>`R`<br>`C`<br>`F` |
| 6 | `Balance` | Balance | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| index | No | LocCode, STAType, STACode |
