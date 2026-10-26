# OBSI - Brazil String Indexer

- **Tabla:** OBSI
- **Descripción:** Brazil String Indexer
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBSI.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IndexType` | Indexer Type | Int | 11 | - |  |  |
| 2 | `Code` | Code | nVarChar | 30 | - |  |  |
| 3 | `Descr` | Beverage Table | Text | 16 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `ID` | Unique ID | Int | 11 | - |  |  |
| 6 | `ValidFrom` | Valid From | Date | 8 | - |  |  |
| 7 | `ValidTo` | Valid To | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
| IND_CODE_K | Yes | IndexType, Code |
