# INV21 - A/R Invoice - Document Reference Information

- **Tabla:** INV21
- **Descripción:** A/R Invoice - Document Reference Information
- **Cantidad de campos:** 21
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/INV21.html

## Campos (21)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ObjectType` | Object Type | nVarChar | 20 | - | 13 |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 4 | `RefType` | Reference Types | VarChar | 1 | - | S | `S` = System Document<br>`E` = External Document |
| 5 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 6 | `RefDocEntr` | Referenced Internal Number | Int | 11 | - |  |  |
| 7 | `RefDocNum` | Referenced Document Number | Int | 11 | - |  |  |
| 8 | `ExtDocNum` | External Referenced Document Number | nVarChar | 100 | - |  |  |
| 9 | `RefObjType` | Referenced Object Type | nVarChar | 20 | - |  | `23` = Sales Quotation<br>`17` = Sales Order<br>`15` = Delivery Notes<br>`234000031` = Return Request<br>`16` = Return<br>`203` = A/R Down Payment<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`165` = A/R Correction Invoice<br>`280` = A/R Tax Invoice<br>`1470000113` = Purchase Request<br>`540000006` = Purchase Quotation<br>`22` = Purchase Order<br>`20` = Goods Receipt PO<br>`234000032` = Goods Return Request<br>`21` = Goods Return<br>`204` = A/P Down Payment<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`163` = A/P Correction Invoice<br>`281` = A/P Tax Invoice<br>`69` = Landed Costs<br>`24` = Incoming Payments<br>`46` = Outgoing Payments<br>`57` = Checks for Payment<br>`321` = Internal Reconciliation<br>`34` = Recurring Posting<br>`30` = Journal Entry<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`162` = Inventory Revaluation<br>`1470000065` = Inventory Counting<br>`10000071` = Inventory Posting<br>`1250000001` = Inventory Transfer Request<br>`67` = Inventory Transfer<br>`202` = Production Order<br>`13001` = Original Invoice<br>`-1` = External Document<br>`20301` = Original Down Payment Invoice |
| 10 | `AccessKey` | Access Key | nVarChar | 100 | - |  |  |
| 11 | `IssueDate` | Date of Issue | Date | 8 | - |  |  |
| 12 | `IssuerCNPJ` | Issuer CNPJ | nVarChar | 100 | - |  |  |
| 13 | `IssuerCode` | Fiscal Document Issuer UF Code | nVarChar | 10 | - |  |  |
| 14 | `Model` | Fiscal Document Model | nVarChar | 6 | - |  |  |
| 15 | `Series` | Fiscal Document Series | nVarChar | 3 | - |  |  |
| 16 | `Number` | Fiscal Document Number | Int | 11 | - |  |  |
| 17 | `RefAccKey` | Referenced CT-e Access Key | nVarChar | 100 | - |  |  |
| 18 | `RefAmount` | Referenced Amount | Num | 19.6 | - |  |  |
| 19 | `SubSeries` | Fiscal Document Subseries | nVarChar | 3 | - |  |  |
| 20 | `Remark` | Remarks | nVarChar | 254 | - |  |  |
| 21 | `LinkRefTyp` | Link Reference Type | nVarChar | 20 | - | 00 | `00`<br>`01` = Nota de cr�dito de los documentos relacionados<br>`02` = Nota de d�bito de los documentos relacionados<br>`03` = Devoluci�n de mercanc�a sobre facturas o traslados previos<br>`04` = Sustituci�n de los CFDI previos<br>`05` = Traslados de mercancias facturados previamente<br>`06` = Factura generada por los traslados previos<br>`07` = CFDI por aplicaci�n de anticipo<br>`08` = Customs<br>`MX_08` = Factura generada por pagos en parcialidades<br>`09` = Factura generada por pagos diferidos |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, RefType |
| DOC_ENTRY | No | DocEntry |
