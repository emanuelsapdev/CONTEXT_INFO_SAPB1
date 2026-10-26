# TPW3 - Utilization and Payment

- **Tabla:** TPW3
- **Descripción:** Utilization and Payment
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TPW3.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Absolute Entry No | Int | 11 | [OTPW](OTPW.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | [TPW2](TPW2.md) |  |  |
| 3 | `CrTaxCtgry` | Credit Tax Category | Int | 11 | - |  |  |
| 4 | `CrTaxType` | Credit Tax Type | Int | 11 | - |  |  |
| 5 | `CrUtiliz` | Credit Utilized Amount | Num | 19.6 | - |  |  |
| 6 | `CrUtilizFC` | Credit Utilized Amount FC | Num | 19.6 | - |  |  |
| 7 | `CrUtilizSC` | Credit Utilized Amount SC | Num | 19.6 | - |  |  |
| 8 | `PymMeth` | Payment Method | nVarChar | 15 | - |  |  |
| 9 | `PymAmnt` | Payment Amount | Num | 19.6 | - |  |  |
| 10 | `PymAmntFC` | Payment Amount (FC) | Num | 19.6 | - |  |  |
| 11 | `PymAmntSC` | Payment Amount (SC) | Num | 19.6 | - |  |  |
| 12 | `MatType` | Material Type | Int | 11 | - | 0 | `0` |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum, CrTaxCtgry, CrTaxType, MatType |
