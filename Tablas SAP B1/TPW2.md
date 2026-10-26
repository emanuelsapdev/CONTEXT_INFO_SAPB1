# TPW2 - Payable Information

- **Tabla:** TPW2
- **Descripción:** Payable Information
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TPW2.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Absolute Entry No | Int | 11 | [OTPW](OTPW.md) |  |  |
| 2 | `LineNumber` | Line Number | Int | 11 | - |  |  |
| 3 | `TaxCategry` | Tax Category | Int | 11 | - |  |  |
| 4 | `TaxType` | Tax Type | Int | 11 | - |  |  |
| 5 | `PyblAmnt` | Payable Amount | Num | 19.6 | - |  |  |
| 6 | `PyblAmntFC` | Payable Amount FC | Num | 19.6 | - |  |  |
| 7 | `PyblAmntSC` | Payable Amount SC | Num | 19.6 | - |  |  |
| 8 | `PLAAmnt` | P.L.A. Amount | Num | 19.6 | - |  |  |
| 9 | `PLAAmntFC` | P.L.A. Amount (FC) | Num | 19.6 | - |  |  |
| 10 | `PLAAmntSC` | P.L.A. Amount (SC) | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNumber |
