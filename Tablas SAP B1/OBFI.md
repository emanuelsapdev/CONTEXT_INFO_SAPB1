# OBFI - Brazil Fuel Indexer

- **Tabla:** OBFI
- **Descripción:** Brazil Fuel Indexer
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBFI.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Fuel Code | nVarChar | 10 | - |  |  |
| 2 | `FGroupCode` | Fuel Group Code | Int | 11 | - |  |  |
| 3 | `Descr` | Description | nVarChar | 254 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `ID` | ID | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
