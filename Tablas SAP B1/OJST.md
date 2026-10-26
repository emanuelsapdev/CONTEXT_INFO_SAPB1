# OJST - TDS Adjustment

- **Tabla:** OJST
- **Descripción:** TDS Adjustment
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OJST.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocDate` | Posting Date | Date | 8 | - |  |  |
| 3 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 4 | `JrnlMemo` | Journal Remarks | nVarChar | 50 | - |  |  |
| 5 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 7 | `UserSign` | User Signature | Int | 11 | [OUSR](OUSR.md) |  |  |
| 8 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 9 | `CreateTime` | Generation Time | Int | 11 | - |  |  |
| 10 | `DepositNum` | Deposit Number | Int | 11 | [OVPM](OVPM.md) |  |  |
| 11 | `CertNum` | Certificate Number | nVarChar | 31 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
