# TPI4 - Purchase Tax Invoice - Linked Down Payments

- **Tabla:** TPI4
- **Descripción:** Purchase Tax Invoice - Linked Down Payments
- **Cantidad de campos:** 23
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TPI4.html

## Campos (23)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ObjType` | Object Type | Int | 11 | - |  |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 4 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 5 | `DpmObjType` | Down Payment Type | Int | 11 | - |  |  |
| 6 | `DpmDocEntr` | Down Payment Entry | Int | 11 | - |  |  |
| 7 | `DpmDocNum` | Down Payment No. | Int | 11 | - |  |  |
| 8 | `PmnObjType` | Payment Type | Int | 11 | - |  |  |
| 9 | `PmnDocEntr` | Payment Entry | Int | 11 | - |  |  |
| 10 | `PmnDocNum` | Payment Number | Int | 11 | - |  |  |
| 11 | `PmnTaxDate` | Payment Date | Date | 8 | - |  |  |
| 12 | `TrsfrDate` | Transfer Date | Date | 8 | - |  |  |
| 13 | `TrsfrRef` | Intended Purpose | nVarChar | 27 | - |  |  |
| 14 | `DrawnSum` | Drawn Amount | Num | 19.6 | - |  |  |
| 15 | `DrawnSumFc` | Drawn Amount (FC) | Num | 19.6 | - |  |  |
| 16 | `DrawnSumSc` | Drawn Amount (SC) | Num | 19.6 | - |  |  |
| 17 | `DocCur` | Document Currency | nVarChar | 3 | - |  |  |
| 18 | `Vat` | Tax Amount | Num | 19.6 | - |  |  |
| 19 | `VatFc` | Tax Amount (FC) | Num | 19.6 | - |  |  |
| 20 | `VatSc` | Tax Amount (SC) | Num | 19.6 | - |  |  |
| 21 | `Gross` | Gross Amount | Num | 19.6 | - |  |  |
| 22 | `GrossFc` | Gross Amount (FC) | Num | 19.6 | - |  |  |
| 23 | `GrossSc` | Gross Amount (SC) | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
| DOC_ENTRY | No | DocEntry |
