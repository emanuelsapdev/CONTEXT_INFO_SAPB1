# OAT1 - Blanket Agreement - Rows

- **Tabla:** OAT1
- **Descripción:** Blanket Agreement - Rows
- **Cantidad de campos:** 38
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OAT1.html

## Campos (38)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AgrNo` | Agreement No. | Int | 11 | [OOAT](OOAT.md) |  |  |
| 2 | `AgrLineNum` | Agreement Row Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `ItemName` | Item Description | nVarChar | 200 | - |  |  |
| 5 | `ItemGroup` | Item Group | Int | 6 | [OITB](OITB.md) |  |  |
| 6 | `PlanQty` | Planned Quantity | Num | 19.6 | - |  |  |
| 7 | `UnitPrice` | Unit Price | Num | 19.6 | - |  |  |
| 8 | `Currency` | Price Currency | nVarChar | 3 | - |  |  |
| 9 | `CumQty` | Cumulative Quantity | Num | 19.6 | - |  |  |
| 10 | `CumAmntFC` | Cumulative Amount in FC | Num | 19.6 | - |  |  |
| 11 | `CumAmntLC` | Cumulative Amount in LC | Num | 19.6 | - |  |  |
| 12 | `FreeTxt` | Free Text | nVarChar | 100 | - |  |  |
| 13 | `InvntryUom` | Inventory UoM | nVarChar | 100 | - |  |  |
| 14 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 15 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 16 | `RetPortion` | Goods Return Probability | Num | 19.6 | - |  |  |
| 17 | `WrrtyEnd` | Date When Goods Expire | Date | 8 | - |  |  |
| 18 | `LineStatus` | Row Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 19 | `PlanAmtLC` | Planned Amount (LC) | Num | 19.6 | - |  |  |
| 20 | `PlanAmtFC` | Planned Amount (FC) | Num | 19.6 | - |  |  |
| 21 | `Discount` | Line Discount | Num | 19.6 | - |  |  |
| 22 | `UomEntry` | UoM Entry | Int | 11 | [OUOM](OUOM.md) |  |  |
| 23 | `UomCode` | UoM Code | nVarChar | 20 | - |  |  |
| 24 | `NumPerMsr` | UoM Value | Num | 19.6 | - | 0 |  |
| 25 | `UndlvQty` | Undeliverd Quantity | Num | 19.6 | - |  |  |
| 26 | `UndlvAmntL` | Undeliverd Amount LC | Num | 19.6 | - |  |  |
| 27 | `UndlvAmntF` | Undeliverd Amount FC | Num | 19.6 | - |  |  |
| 28 | `TrnspCode` | Shipping Type | Int | 6 | [OSHP](OSHP.md) |  |  |
| 29 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 30 | `TaxCode` | Tax Code | nVarChar | 8 | - |  |  |
| 31 | `TAXRate` | TAX Rate | Num | 19.6 | - |  |  |
| 32 | `PlVatAmtLC` | Planned VAT Amount (LC) | Num | 19.6 | - |  |  |
| 33 | `PlVatAmtFC` | Planned VAT Amount (FC) | Num | 19.6 | - |  |  |
| 34 | `CumVtAmtLC` | Cumulative VAT Amount (LC) | Num | 19.6 | - |  |  |
| 35 | `CumVtAmtFC` | Cumulative VAT Amount (FC) | Num | 19.6 | - |  |  |
| 36 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 37 | `UoMNum` | UoM Item Per Unit Numerator | Num | 19.6 | - |  |  |
| 38 | `UoMDen` | UoM Item Per Unit Denominator | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AgrNo, AgrLineNum |
