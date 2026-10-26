# OADP - Print Preferences

- **Tabla:** OADP
- **Descripción:** Print Preferences
- **Cantidad de campos:** 45
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OADP.html

## Campos (45)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PrintId` | Print Number | nVarChar | 4 | - |  |  |
| 2 | `ObjList` | Object List | nVarChar | 11 | - | 13 | `1470000049` = Capitalization<br>`1470000071` = Depreciation Run<br>`1470000090` = Fixed Asset Transfer<br>`23` = Sales Quotation<br>`17` = Sales Order<br>`15` = Delivery<br>`234000031` = Return Request<br>`16` = Returns<br>`203` = A/R Down Payment<br>`13` = A/R Invoice<br>`165` = A/R Correction Invoice<br>`166` = A/R Correction Invoice Reversal<br>`14` = A/R Credit Memo<br>`270` = A/R Monthly Invoice<br>`1470000113` = Purchase Request<br>`540000006` = Purchase Quotation<br>`22` = Purchase Order<br>`20` = Goods Receipt PO<br>`234000032` = Goods Return Request<br>`21` = Goods Return<br>`204` = A/P Down Payment<br>`18` = A/P Invoice<br>`163` = A/P Correction Invoice<br>`164` = A/P Correction Invoice Reversal<br>`19` = A/P Credit Memo<br>`140000014` = A/P Monthly Invoice<br>`69` = Landed Costs<br>`24` = Incoming Payment<br>`25` = Deposit<br>`46` = Outgoing Payment<br>`76` = Postdated Deposit<br>`57` = Check for Payment<br>`30` = Journal Entry<br>`28` = Journal Voucher<br>`140000010` = Incoming Excise Invoice<br>`140000009` = Outgoing Excise Invoice<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`1250000001` = Inventory Transfer Request<br>`67` = Inventory Transfer<br>`68` = Work Instructions<br>`202` = Production Order<br>`162` = Inventory Revaluation<br>`156` = Pick List<br>`1470000065` = Inventory Counting<br>`10000071` = Inventory Posting<br>`310000001` = Inventory Opening Balances<br>`191` = Service Call<br>`190` = Service Contract<br>`176` = Equipment Card<br>`88` = Entrada<br>`89` = Salida<br>`90` = Traspaso<br>`132` = Correction Invoice<br>`234000021` = Project Management Document |
| 3 | `MaxLineNum` | Max. Rows per Page | Int | 6 | - | 99 |  |
| 4 | `TopMrgn` | Top Margin Width | Int | 6 | - |  |  |
| 5 | `BtmMrgn` | Bottom Margin Width | Int | 6 | - |  |  |
| 6 | `LftMrgn` | Left Margin Width | Int | 6 | - |  |  |
| 7 | `RgtMrgn` | Right Margin Width | Int | 6 | - |  |  |
| 8 | `PrnCompany` | Print on Company Paper | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `MnhlNote` | Text Printed by PLD | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 10 | `MaxWordLin` | Max. Rows for Export | Int | 6 | - | 10 |  |
| 11 | `V_Compress` | Compress Vertically | Int | 6 | - | 100 | `50` = 50<br>`60` = 60<br>`70` = 70<br>`80` = 80<br>`90` = 90<br>`100` = 100<br>`110` = 110<br>`120` = 120<br>`130` = 130<br>`140` = 140<br>`150` = 150 |
| 12 | `WordPath` | WORD Template Path | Text | 16 | - |  |  |
| 13 | `BitmapPath` | Picture Path | Text | 16 | - |  |  |
| 14 | `PrintMeta` | Print as Picture | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `PrintRcpt` | Print Receipt | VarChar | 1 | - | N | `N` = No<br>`A` = Only When Adding<br>`Y` = Always |
| 16 | `ShortRcpt` | Print Payment with Invoice | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 17 | `ExportCode` | Export Material/Account Code | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `AttachPath` | Attachments Path | Text | 16 | - |  |  |
| 19 | `DraftNote` | Print Draft Note | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 20 | `ExtPath` | Extensions Path | Text | 16 | - |  |  |
| 21 | `DmePath` | DME Files Store Path | Text | 16 | - |  |  |
| 22 | `SNType` | Serial Number Type | Int | 6 | - | 2 | `1` = Mfr Serial No.<br>`2` = Serial No.<br>`3` = Lot Number |
| 23 | `GBIPath` | GB Data Interface Path | Text | 16 | - |  |  |
| 24 | `LogoFile` | Logo File | nVarChar | 200 | - |  |  |
| 25 | `LogoImage` | Logo Image | Text | 16 | - |  |  |
| 26 | `B1Server` | Business One Server Address | Text | 16 | - |  |  |
| 27 | `IsTrustSrv` | Always Trust This Server | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 28 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 29 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 30 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 31 | `SnapShotId` | Snapshot ID | Int | 11 | - | 0 |  |
| 32 | `DefirExpP` | Export Folder | Text | 16 | - |  |  |
| 33 | `DefirDemop` | DEFIR Database Path | Text | 16 | - |  |  |
| 34 | `PrintPDF` | Generate PDF When Printing | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 35 | `PrtCancel` | Print Watermark on Cancl. Docs | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 36 | `PrtUseSys` | Use System Print Preferences | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 37 | `RptList` | Report List | nVarChar | 20 | - | 1 | `1` = Aging Report<br>`2` = Dunning Wizard |
| 38 | `PreAttach` | Previous Attachment Path | Text | 16 | - |  |  |
| 39 | `ExportPDF` | Export PDF to Dflt Attachment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 40 | `AttachPDF` | Attach Exported PDF to Doc | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 41 | `GSTPath` | GST ANX Report Path | Text | 16 | - |  |  |
| 42 | `CRNote` | Text Printed by Crystal Reports | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 43 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 44 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 45 | `GSTRtnPath` | GST Return Path | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PrintId |
