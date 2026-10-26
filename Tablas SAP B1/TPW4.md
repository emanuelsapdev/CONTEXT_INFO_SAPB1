# TPW4 - VAT Refund

- **Tabla:** TPW4
- **Descripción:** VAT Refund
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TPW4.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Absolute Entry No | Int | 11 | [OTPW](OTPW.md) |  |  |
| 2 | `RefundAcct` | Refund Account Code | nVarChar | 15 | - |  |  |
| 3 | `RefundAmnt` | Refund Amount | Num | 19.6 | - |  |  |
| 4 | `RfndAmntFC` | Refund Amount FC | Num | 19.6 | - |  |  |
| 5 | `RfndAmntSC` | Refund Amount SC | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
