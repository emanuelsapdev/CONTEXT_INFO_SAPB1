# RDR25 - Sales Order - Amt Per VAT Grp

- **Tabla:** RDR25
- **Descripción:** Sales Order - Amt Per VAT Grp
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RDR25.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | ODOC |  |  |
| 2 | `VatGroup` | Tax Definition | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 3 | `VatPrcnt` | Tax Rate | Num | 19.6 | - |  |  |
| 4 | `BaseAmnt` | Base Amount | Num | 19.6 | - |  |  |
| 5 | `BaseAmntFC` | Base Amount (FC) | Num | 19.6 | - |  |  |
| 6 | `BaseAmntSC` | Base Amount (SC) | Num | 19.6 | - |  |  |
| 7 | `VatSum` | Tax Amount | Num | 19.6 | - |  |  |
| 8 | `VatSumFrgn` | Tax Amount (FC) | Num | 19.6 | - |  |  |
| 9 | `VatSumSy` | Tax Amount (SC) | Num | 19.6 | - |  |  |
| 10 | `Type` | Type | Int | 11 | - | 1 | `1` = Discount by Tax |
| 11 | `Currency` | Price Currency | nVarChar | 3 | - |  |  |
| 12 | `Rate` | Currency Rate | Num | 19.6 | - |  |  |
| 13 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 14 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 17 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, VatGroup, Type |
