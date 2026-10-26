# SVR1 - Saved Reconciliations - Transaction List

- **Tabla:** SVR1
- **Descripción:** Saved Reconciliations - Transaction List
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SVR1.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `acctCode` | Account Code | nVarChar | 15 | - |  |  |
| 2 | `transID` | Transaction ID | Int | 11 | [OJDT](OJDT.md) |  |  |
| 3 | `transLine` | Transaction Row | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | acctCode, transID, transLine |
