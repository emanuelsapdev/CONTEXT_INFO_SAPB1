# OBBI - Brazil Beverage Indexer

- **Tabla:** OBBI
- **Descripción:** Brazil Beverage Indexer
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBBI.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TableCode` | Beverage Table Code | nVarChar | 2 | [OBSI](OBSI.md) |  |  |
| 2 | `BrandCode` | Beverage Commercial Brand Code | Int | 11 | [OBNI](OBNI.md) |  |  |
| 3 | `GroupCode` | Beverage Group Code | nVarChar | 2 | [OBSI](OBSI.md) |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `ID` | ID | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
| TBL_TM_GRP | Yes | TableCode, BrandCode, GroupCode |
