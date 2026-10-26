# OBCG - Bank Charge for Bank Transfers

- **Tabla:** OBCG
- **Descripción:** Bank Charge for Bank Transfers
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBCG.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CardCode` | BP Code | nVarChar | 15 | - |  |  |
| 2 | `BkChgAmt` | Bank Charge | Num | 19.6 | - |  |  |
| 3 | `SerialNo` | Serial No. | Int | 11 | - |  |  |
| 4 | `DocCurr` | Document Currency | nVarChar | 3 | - |  |  |
| 5 | `BcgTaxAmt` | Bank Charge Tax | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SerialNo |
