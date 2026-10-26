# WTM3 - Approval Templates - Documents

- **Tabla:** WTM3
- **Descripción:** Approval Templates - Documents
- **Cantidad de campos:** 2
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WTM3.html

## Campos (2)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WtmCode` | Code | Int | 11 | [OWTM](OWTM.md) |  |  |
| 2 | `TransType` | Original Document | nVarChar | 20 | - |  | `23` = Sales Quotation<br>`17` = Sales Order<br>`15` = Delivery<br>`234000031` = Returns Request<br>`16` = Returns<br>`203` = A/R Down Payment<br>`13` = A/R Invoice<br>`165` = A/R Correction Invoice<br>`166` = A/R Correction Invoice Reversal<br>`14` = A/R Credit Memo<br>`132` = Correction Invoice<br>`1470000113` = Purchase Request<br>`540000006` = Purchase Quotation<br>`22` = Purchase Order<br>`20` = Goods Receipt PO<br>`234000032` = Goods Returns Request<br>`21` = Goods Returns<br>`204` = A/P Down Payment<br>`18` = A/P Invoice<br>`163` = A/P Correction Invoice<br>`164` = A/P Correction Invoice Reversal<br>`19` = A/P Credit Memo<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`1250000001` = Inventory Transfer Request<br>`67` = Inventory Transfer<br>`1470000065` = Inventory Counting<br>`310000001` = Inventory Opening Balance<br>`10000071` = Inventory Posting<br>`46` = Outgoing Payment<br>`1250000026` = Sales Blanket Agreements<br>`1250000027` = Purchase Blanket Agreements |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WtmCode, TransType |
