# SRA1 - Scheduled Report Parameters

- **Tabla:** SRA1
- **Descripción:** Scheduled Report Parameters
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SRA1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ActionCode` | Action Code | Int | 11 | - |  |  |
| 2 | `ParamCode` | Parameter Code | Int | 11 | - |  |  |
| 3 | `KeyString` | Parameter Key String | nVarChar | 32 | - |  |  |
| 4 | `KeyNumber` | Parameter Key Numerator | Int | 11 | - |  |  |
| 5 | `ValString` | Parameter Value String | Text | 16 | - |  |  |
| 6 | `ValNumber` | Parameter Value Number | Int | 11 | - |  |  |
| 7 | `ValMoney` | Parameter Value Money | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ActionCode, ParamCode |
| SECONDARY | Yes | ActionCode, KeyString, KeyNumber |
