# OBNI - Brazil Numeric Indexer

- **Tabla:** OBNI
- **Descripción:** Brazil Numeric Indexer
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBNI.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IndexType` | Indexer Type | Int | 11 | - |  |  |
| 2 | `Code` | Code | Int | 11 | - |  |  |
| 3 | `Descr` | Beverage Brand | nVarChar | 254 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `ID` | ID | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
| IND_CODE_K | Yes | IndexType, Code |
