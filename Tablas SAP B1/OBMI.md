# OBMI - Brazilian Multi-Indexer

- **Tabla:** OBMI
- **Descripción:** Brazilian Multi-Indexer
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBMI.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ID` | Unique ID | Int | 11 | - |  |  |
| 2 | `IndexType` | Indexer Type | Int | 11 | - | -1 |  |
| 3 | `Code` | Code | nVarChar | 10 | - |  |  |
| 4 | `Descr` | Description | nVarChar | 254 | - |  |  |
| 5 | `RefIndCod1` | First Referenced Indexer Code | nVarChar | 10 | - |  |  |
| 6 | `RefIndCod2` | Second Referenced Indexer Code | nVarChar | 10 | - |  |  |
| 7 | `RefIndCod3` | Third Referenced Indexer Code | nVarChar | 10 | - |  |  |
| 8 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
| IND_CODE_K | Yes | IndexType, Code |
