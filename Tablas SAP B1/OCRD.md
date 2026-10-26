# OCRD - Business Partners

- **Tabla:** OCRD
- **Descripción:** Business Partners
- **Cantidad de campos:** 396
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCRD.html

## Campos (396)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CardCode` | BP Code | nVarChar | 15 | - |  |  |
| 2 | `CardName` | BP Name | nVarChar | 200 | - |  |  |
| 3 | `CardType` | BP Type | VarChar | 1 | - | C | `C` = Customer<br>`S` = Vendor<br>`L` = Lead |
| 4 | `GroupCode` | Group Code | Int | 6 | [OCRG](OCRG.md) |  |  |
| 5 | `CmpPrivate` | Type of Business | VarChar | 1 | - | C | `C` = Company<br>`I` = Private<br>`G` = Government<br>`E` = Employee<br>`S` = Sole Taxable Subject |
| 6 | `Address` | Bill-to Street | nVarChar | 100 | - |  |  |
| 7 | `ZipCode` | Bill-to Zip Code | nVarChar | 20 | - |  |  |
| 8 | `MailAddres` | Ship-to Street | nVarChar | 100 | - |  |  |
| 9 | `MailZipCod` | Ship-to Zip Code | nVarChar | 20 | - |  |  |
| 10 | `Phone1` | Telephone 1 | nVarChar | 50 | - |  |  |
| 11 | `Phone2` | Telephone 2 | nVarChar | 50 | - |  |  |
| 12 | `Fax` | Fax Number | nVarChar | 50 | - |  |  |
| 13 | `CntctPrsn` | Contact Person | nVarChar | 90 | - |  |  |
| 14 | `Notes` | Remarks | nVarChar | 100 | - |  |  |
| 15 | `Balance` | Account Balance | Num | 19.6 | - |  |  |
| 16 | `ChecksBal` | Open Checks Balance in FC | Num | 19.6 | - |  |  |
| 17 | `DNotesBal` | Open Deliveries/GRPO Balance | Num | 19.6 | - |  |  |
| 18 | `OrdersBal` | Open Orders Balance | Num | 19.6 | - |  |  |
| 19 | `GroupNum` | Payment Terms Code | Int | 6 | [OCTG](OCTG.md) | -1 |  |
| 20 | `CreditLine` | Credit Limit | Num | 19.6 | - |  |  |
| 21 | `DebtLine` | Payable Limit | Num | 19.6 | - |  |  |
| 22 | `Discount` | Discount % | Num | 19.6 | - |  |  |
| 23 | `VatStatus` | Tax Definition | VarChar | 1 | - | Y | `Y` = Liable<br>`N` = Exempted<br>`E` = EU |
| 24 | `LicTradNum` | Federal Tax ID | nVarChar | 32 | - |  |  |
| 25 | `DdctStatus` | Liable for Ded. at Source | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 26 | `DdctPrcnt` | Withholding Tax Deduction % | Num | 19.6 | - |  |  |
| 27 | `ValidUntil` | Expiration Date for -% of Deduction | Date | 8 | - |  |  |
| 28 | `Chrctrstcs` | Properties | Int | 11 | - |  |  |
| 29 | `ExMatchNum` | Last Ext. Reconciliation No. | Int | 11 | - |  |  |
| 30 | `InMatchNum` | Last Int. Reconciliation No. | Int | 11 | - |  |  |
| 31 | `ListNum` | Price List No. | Int | 6 | [OPLN](OPLN.md) |  |  |
| 32 | `DNoteBalFC` | Open DN Balance in BP Curr. | Num | 19.6 | - |  |  |
| 33 | `OrderBalFC` | Open Orders Bal. in BP Curr. | Num | 19.6 | - |  |  |
| 34 | `DNoteBalSy` | Open Deliveries/GRPO Balance in SC | Num | 19.6 | - |  |  |
| 35 | `OrderBalSy` | Open Orders Balance in SC | Num | 19.6 | - |  |  |
| 36 | `Transfered` | Year Transfer | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 37 | `BalTrnsfrd` | Balances transferred | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 38 | `IntrstRate` | Interest % on Liabilities | Num | 19.6 | - |  |  |
| 39 | `Commission` | Commission % for Customer | Num | 19.6 | - |  |  |
| 40 | `CommGrCode` | Commission Group | Int | 6 | [OCOG](OCOG.md) | 0 |  |
| 41 | `Free_Text` | Free Text | Text | 16 | - |  |  |
| 42 | `SlpCode` | Sales Employee Code | Int | 11 | [OSLP](OSLP.md) | -1 |  |
| 43 | `PrevYearAc` | Previous Year Balance | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 44 | `Currency` | BP Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 45 | `RateDifAct` | Rate Differences Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 46 | `BalanceSys` | Account Balance in SC | Num | 19.6 | - |  |  |
| 47 | `BalanceFC` | BP Balance in FC | Num | 19.6 | - |  |  |
| 48 | `Protected` | Protected BP | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 49 | `Cellular` | Mobile Phone | nVarChar | 50 | - |  |  |
| 50 | `AvrageLate` | Average Payment Delay in Days | Int | 6 | - |  |  |
| 51 | `City` | Bill-to City | nVarChar | 100 | - |  |  |
| 52 | `County` | Bill-to County | nVarChar | 100 | - |  |  |
| 53 | `Country` | Bill-to Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 54 | `MailCity` | Ship-to City | nVarChar | 100 | - |  |  |
| 55 | `MailCounty` | Ship-to County | nVarChar | 100 | - |  |  |
| 56 | `MailCountr` | Ship-to Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 57 | `E_Mail` | E-Mail | nVarChar | 100 | - |  |  |
| 58 | `Picture` | Picture | nVarChar | 200 | - |  |  |
| 59 | `DflAccount` | Default Account | nVarChar | 50 | - |  |  |
| 60 | `DflBranch` | Default Branch | nVarChar | 50 | - |  |  |
| 61 | `BankCode` | Default Bank | nVarChar | 30 | - | -1 |  |
| 62 | `AddID` | ID No. 2 | nVarChar | 64 | - |  |  |
| 63 | `Pager` | Pager | nVarChar | 30 | - |  |  |
| 64 | `FatherCard` | Consolidating Business Partner | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 65 | `CardFName` | Foreign Name | nVarChar | 200 | - |  |  |
| 66 | `FatherType` | Parent Summary Type | VarChar | 1 | - | P | `P` = Payment Consolidation<br>`D` = Delivery Consolidation |
| 67 | `QryGroup1` | Property 1 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 68 | `QryGroup2` | Property 2 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 69 | `QryGroup3` | Property 3 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 70 | `QryGroup4` | Property 4 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 71 | `QryGroup5` | Property 5 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 72 | `QryGroup6` | Property 6 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 73 | `QryGroup7` | Property 7 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 74 | `QryGroup8` | Property 8 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 75 | `QryGroup9` | Property 9 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 76 | `QryGroup10` | Property 10 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 77 | `QryGroup11` | Property 11 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 78 | `QryGroup12` | Property 12 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 79 | `QryGroup13` | Property 13 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 80 | `QryGroup14` | Property 14 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 81 | `QryGroup15` | Property 15 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 82 | `QryGroup16` | Property 16 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 83 | `QryGroup17` | Property 17 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 84 | `QryGroup18` | Property 18 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 85 | `QryGroup19` | Property 19 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 86 | `QryGroup20` | Property 20 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 87 | `QryGroup21` | Property 21 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 88 | `QryGroup22` | Property 22 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 89 | `QryGroup23` | Property 23 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 90 | `QryGroup24` | Property 24 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 91 | `QryGroup25` | Property 25 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 92 | `QryGroup26` | Property 26 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 93 | `QryGroup27` | Property 27 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 94 | `QryGroup28` | Property 28 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 95 | `QryGroup29` | Property 29 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 96 | `QryGroup30` | Property 30 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 97 | `QryGroup31` | Property 31 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 98 | `QryGroup32` | Property 32 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 99 | `QryGroup33` | Property 33 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 100 | `QryGroup34` | Property 34 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 101 | `QryGroup35` | Property 35 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 102 | `QryGroup36` | Property 36 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 103 | `QryGroup37` | Property 37 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 104 | `QryGroup38` | Property 38 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 105 | `QryGroup39` | Property 39 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 106 | `QryGroup40` | Property 40 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 107 | `QryGroup41` | Property 41 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 108 | `QryGroup42` | Property 42 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 109 | `QryGroup43` | Property 43 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 110 | `QryGroup44` | Property 44 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 111 | `QryGroup45` | Property 45 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 112 | `QryGroup46` | Property 46 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 113 | `QryGroup47` | Property 47 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 114 | `QryGroup48` | Property 48 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 115 | `QryGroup49` | Property 49 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 116 | `QryGroup50` | Property 50 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 117 | `QryGroup51` | Property 51 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 118 | `QryGroup52` | Property 52 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 119 | `QryGroup53` | Property 53 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 120 | `QryGroup54` | Property 54 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 121 | `QryGroup55` | Property 55 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 122 | `QryGroup56` | Property 56 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 123 | `QryGroup57` | Property 57 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 124 | `QryGroup58` | Property 58 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 125 | `QryGroup59` | Property 59 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 126 | `QryGroup60` | Property 60 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 127 | `QryGroup61` | Property 61 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 128 | `QryGroup62` | Property 62 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 129 | `QryGroup63` | Property 63 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 130 | `QryGroup64` | Property 64 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 131 | `DdctOffice` | Deduction Approval Office | nVarChar | 10 | - |  |  |
| 132 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 133 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 134 | `ExportCode` | Data Export Code | nVarChar | 8 | - |  |  |
| 135 | `DscntObjct` | Object for Discounts | Int | 6 | - | -1 | `-1`<br>`52` = Groups<br>`8` = Properties<br>`43` = Companies<br>`4` = Items |
| 136 | `DscntRel` | Discounts Ratio | VarChar | 1 | - | L | `L` = Lowest Discount<br>`H` = Highest Discount<br>`A` = Average Disc.<br>`S` = Discount Totals<br>`M` = Discount Multiples |
| 137 | `SPGCounter` | SPG Counter | Int | 6 | - | 0 |  |
| 138 | `SPPCounter` | SPP Counter | Int | 11 | - | 0 |  |
| 139 | `DdctFileNo` | Tax Deduction File Number | nVarChar | 9 | - |  |  |
| 140 | `SCNCounter` | SCN Counter | Int | 6 | - |  |  |
| 141 | `MinIntrst` | Min. Interest Letter Amount | Num | 19.6 | - |  |  |
| 142 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 143 | `OprCount` | Open Opportunities | Int | 11 | - |  |  |
| 144 | `ExemptNo` | Exempt No. | nVarChar | 50 | - |  |  |
| 145 | `Priority` | Priority | Int | 11 | [OBPP](OBPP.md) | -1 |  |
| 146 | `CreditCard` | Credit Cards | Int | 6 | [OCRC](OCRC.md) | -1 |  |
| 147 | `CrCardNum` | Credit Card No. | nVarChar | 254 | - |  |  |
| 148 | `CardValid` | Credit Card Validity | Date | 8 | - |  |  |
| 149 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 150 | `LocMth` | LC Reconciliation | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 151 | `validFor` | Active | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 152 | `validFrom` | Active From | Date | 8 | - |  |  |
| 153 | `validTo` | Active To | Date | 8 | - |  |  |
| 154 | `frozenFor` | Inactive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 155 | `frozenFrom` | Inactive From | Date | 8 | - |  |  |
| 156 | `frozenTo` | Inactive To | Date | 8 | - |  |  |
| 157 | `sEmployed` | Self-Employed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 158 | `MTHCounter` | MTH Counter | Int | 11 | - |  |  |
| 159 | `BNKCounter` | BNK Counter | Int | 11 | - |  |  |
| 160 | `DdgKey` | Withholding Tax Deduction Grp | Int | 11 | [ODDG](ODDG.md) | -1 |  |
| 161 | `DdtKey` | Current Deduction Hierarchy | Int | 11 | - | -1 |  |
| 162 | `ValidComm` | Active Remarks | nVarChar | 30 | - |  |  |
| 163 | `FrozenComm` | Inactive Remarks | nVarChar | 30 | - |  |  |
| 164 | `chainStore` | Belongs to Retail Store | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 165 | `DiscInRet` | Allow Doc Discount in Returns | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 166 | `State1` | Bill-to State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 167 | `State2` | Ship-to State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 168 | `VatGroup` | Tax Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 169 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 170 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 2 |  |
| 171 | `Indicator` | Indicator | nVarChar | 2 | [OIDC](OIDC.md) |  |  |
| 172 | `ShipType` | Shipping Type | Int | 6 | [OSHP](OSHP.md) |  |  |
| 173 | `DebPayAcct` | Accounts Receivable/Payable | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 174 | `ShipToDef` | Ship-to-Default | nVarChar | 50 | - |  |  |
| 175 | `Block` | Bill-to Block | nVarChar | 100 | - |  |  |
| 176 | `MailBlock` | Ship-to Block | nVarChar | 100 | - |  |  |
| 177 | `Password` | Password | nVarChar | 32 | - |  |  |
| 178 | `ECVatGroup` | Tax Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 179 | `Deleted` | Deleted | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 180 | `IBAN` | IBAN | nVarChar | 50 | - |  |  |
| 181 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 182 | `FormCode` | 1099 Form Code | Int | 11 | [OTNN](OTNN.md) |  |  |
| 183 | `Box1099` | 1099 Box | nVarChar | 20 | - |  |  |
| 184 | `PymCode` | Payment Method Code | nVarChar | 15 | [OPYM](OPYM.md) | -1 |  |
| 185 | `BackOrder` | Backorder | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 186 | `PartDelivr` | Partial Delivery | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 187 | `DunnLevel` | Dunning Level | Int | 11 | [ODUN](ODUN.md) |  |  |
| 188 | `DunnDate` | Dunning Date | Date | 8 | - |  |  |
| 189 | `BlockDunn` | Block Dunning | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 190 | `BankCountr` | Bank Country | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 191 | `CollecAuth` | Collection Authorization | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 192 | `DME` | DME Identification | nVarChar | 5 | - |  |  |
| 193 | `InstrucKey` | Instruction Key | nVarChar | 30 | - |  |  |
| 194 | `SinglePaym` | Single Payment | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 195 | `ISRBillId` | ISR Biller ID | nVarChar | 9 | - |  |  |
| 196 | `PaymBlock` | Payment Block | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 197 | `RefDetails` | Reference Details | nVarChar | 20 | - |  |  |
| 198 | `HouseBank` | House Bank | nVarChar | 30 | - | -1 |  |
| 199 | `OwnerIdNum` | ID Number | nVarChar | 15 | - |  |  |
| 200 | `PyBlckDesc` | Payment Block Description | Int | 11 | [OPYB](OPYB.md) | -1 |  |
| 201 | `HousBnkCry` | House Bank Country | nVarChar | 3 | - |  |  |
| 202 | `HousBnkAct` | House Bank Account | nVarChar | 50 | - |  |  |
| 203 | `HousBnkBrn` | House Bank Branch | nVarChar | 50 | - |  |  |
| 204 | `ProjectCod` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 205 | `SysMatchNo` | Last Sys. Reconciliation No. | Int | 11 | - | -1 |  |
| 206 | `VatIdUnCmp` | Unified Federal Tax ID | nVarChar | 32 | - |  |  |
| 207 | `AgentCode` | Agent Code | nVarChar | 32 | [OAGP](OAGP.md) |  |  |
| 208 | `TolrncDays` | Tolerance Days | Int | 6 | - |  |  |
| 209 | `SelfInvoic` | Self Invoice | VarChar | 1 | - |  |  |
| 210 | `DeferrTax` | Deferred Tax | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 211 | `LetterNum` | Tax Exemption Letter No. | nVarChar | 50 | - |  |  |
| 212 | `MaxAmount` | Max. Exemption Amount | Num | 19.6 | - |  |  |
| 213 | `FromDate` | Exemption Validity Date From | Date | 8 | - |  |  |
| 214 | `ToDate` | Exemption Validity Date To | Date | 8 | - |  |  |
| 215 | `WTLiable` | Subject to Withholding Tax | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No<br>None |
| 216 | `CrtfcateNO` | Certificate No. | nVarChar | 20 | - |  |  |
| 217 | `ExpireDate` | Expiration Date | Date | 8 | - |  |  |
| 218 | `NINum` | Registration No. | nVarChar | 20 | - |  |  |
| 219 | `AccCritria` | Accrual | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 220 | `WTCode` | WTax Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 221 | `Equ` | Equalization Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 222 | `HldCode` | Holidays Name | nVarChar | 20 | [OHLD](OHLD.md) |  |  |
| 223 | `ConnBP` | Linked Business Partner | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 224 | `MltMthNum` | Last Multi. Reconciliation No. | Int | 11 | - |  |  |
| 225 | `TypWTReprt` | BP Type for WTax Report | VarChar | 1 | - | C | `C` = Company<br>`P` = Person |
| 226 | `VATRegNum` | VAT Reg. Number | nVarChar | 32 | - |  |  |
| 227 | `RepName` | Representative Name | nVarChar | 15 | - |  |  |
| 228 | `Industry` | Industry | Text | 16 | - |  |  |
| 229 | `Business` | Business | Text | 16 | - |  |  |
| 230 | `WTTaxCat` | Withholding Tax Cat. | Text | 16 | - |  |  |
| 231 | `IsDomestic` | Is Domestic | VarChar | 1 | - | Y | `Y` = Domestic<br>`N` = Foreign |
| 232 | `IsResident` | Is Resident | VarChar | 1 | - | Y | `Y` = Resident<br>`N` = Non-Resident |
| 233 | `AutoCalBCG` | Auto Calculated Bank Charges | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 234 | `OtrCtlAcct` | Other Receivable/Payable | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 235 | `AliasName` | Alias Name | Text | 16 | - |  |  |
| 236 | `Building` | Bill-to Building/Floor/Room | Text | 16 | - |  |  |
| 237 | `MailBuildi` | Ship to Building/Floor/Room | Text | 16 | - |  |  |
| 238 | `BoEPrsnt` | Customer Bill of Exchang Pres | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 239 | `BoEDiscnt` | Customer BoE Discounted | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 240 | `BoEOnClct` | Bill of Exchange on Collection | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 241 | `UnpaidBoE` | Unpaid Bill of Exchange | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 242 | `ITWTCode` | Income Tax WTax Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 243 | `DunTerm` | Dunning Term | nVarChar | 25 | [ODUT](ODUT.md) |  |  |
| 244 | `ChannlBP` | Channel BP | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 245 | `DfTcnician` | Default Technician | Int | 11 | [OHEM](OHEM.md) |  |  |
| 246 | `Territory` | Territory | Int | 11 | [OTER](OTER.md) |  |  |
| 247 | `BillToDef` | Bill-to Default | nVarChar | 50 | - |  |  |
| 248 | `DpmClear` | Payment Advances | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 249 | `IntrntSite` | Web Site | nVarChar | 100 | - |  |  |
| 250 | `LangCode` | Language Code | Int | 11 | [OLNG](OLNG.md) |  |  |
| 251 | `HousActKey` | House Bank Account Key | Int | 11 | [DSC1](DSC1.md) |  |  |
| 252 | `Profession` | Profession | nVarChar | 50 | - |  |  |
| 253 | `CDPNum` | Closing Date Procedure Number | Int | 6 | [OCDP](OCDP.md) |  |  |
| 254 | `DflBankKey` | Default Bank Key | Int | 11 | [ODSC](ODSC.md) |  |  |
| 255 | `BCACode` | Bank Charges Allocation Codes | nVarChar | 3 | [OBCA](OBCA.md) |  |  |
| 256 | `UseShpdGd` | Use Shipped Goods Account | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 257 | `RegNum` | Company Reg. No. (CRN) | nVarChar | 32 | - |  |  |
| 258 | `VerifNum` | WTax Verification No. | nVarChar | 32 | - |  |  |
| 259 | `BankCtlKey` | Default Bank Internal ID | nVarChar | 2 | - |  |  |
| 260 | `HousCtlKey` | House Bank Control Number | nVarChar | 2 | - |  |  |
| 261 | `AddrType` | Bill-to Address Type | nVarChar | 100 | - |  |  |
| 262 | `InsurOp347` | 347 Insurance Operation | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 263 | `MailAddrTy` | Ship-to Address Type | nVarChar | 100 | - |  |  |
| 264 | `StreetNo` | Bill-to Street No. | nVarChar | 100 | - |  |  |
| 265 | `MailStrNo` | Ship-to Street No. | nVarChar | 100 | - |  |  |
| 266 | `TaxRndRule` | Tax Rounding Rule | VarChar | 1 | - | D | `D` = Company Default<br>`R` = Round Off<br>`C` = Round Up<br>`F` = Round Down |
| 267 | `VendTID` | Vender Type ID | Int | 11 | [OVTP](OVTP.md) |  |  |
| 268 | `ThreshOver` | Threshold Overlook | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 269 | `SurOver` | Surcharge Overlook | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 270 | `VendorOcup` | Vendor Occupation | nVarChar | 15 | - |  |  |
| 271 | `OpCode347` | 347 Operation Code | VarChar | 1 | - |  | `A` = Goods or Services Acquisitions<br>`D` = Public Entities Acquisitions<br>`G` = Travel Agent Purchases<br>`B` = Sales or Services Revenues<br>`E` = Public Subsidies<br>`F` = Travel Agent Sales |
| 272 | `DpmIntAct` | DPM Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 273 | `ResidenNum` | Residence Number | VarChar | 1 | - | 1 | `1` = Spanish Fiscal ID<br>`2` = VAT Registration Number<br>`3` = Passport<br>`4` = Fiscal ID Issued by the Country of Residence<br>`5` = Certificate of Fiscal Residence<br>`6` = Other Document<br>`7` = Not Registered |
| 274 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 275 | `PlngGroup` | Planning Group | nVarChar | 10 | - |  |  |
| 276 | `VatIDNum` | VAT ID Number | nVarChar | 32 | - |  |  |
| 277 | `Affiliate` | Affiliate | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 278 | `MivzExpSts` | Mivzak Export Status | VarChar | 1 | - | B | `B` = Not Exported<br>`U` = Exported<br>`D` = Deleted |
| 279 | `HierchDdct` | Hierarchical Deduction | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 280 | `CertWHT` | Withholding Tax Certified | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 281 | `CertBKeep` | Bookkeeping Certified | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 282 | `WHShaamGrp` | Withholding Shaam Group | VarChar | 1 | - | 1 | `1` = Services and Agriculture Products<br>`2` = Construction and Transportation<br>`3` = Insurance Commissions<br>`4` = Withholding Tax Instructions<br>`5` = Interest Exchange Rate Differences<br>`6` = Rental Fees |
| 283 | `IndustryC` | Industry | Int | 11 | [OOND](OOND.md) |  |  |
| 284 | `DatevAcct` | DATEV Account | nVarChar | 9 | - |  |  |
| 285 | `DatevFirst` | First Data Entry | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 286 | `GTSRegNum` | GTS Registration Number | nVarChar | 20 | - |  |  |
| 287 | `GTSBankAct` | GTS Bank Account | nVarChar | 80 | - |  |  |
| 288 | `GTSBilAddr` | GTS Billing Address | nVarChar | 80 | - |  |  |
| 289 | `HsBnkSwift` | House Bank BIC/SWIFT Code | nVarChar | 50 | - |  |  |
| 290 | `HsBnkIBAN` | House Bank IBAN | nVarChar | 50 | - |  |  |
| 291 | `DflSwift` | Default Bank BIC/SWIFT Code | nVarChar | 50 | - |  |  |
| 292 | `AutoPost` | Automatic Posting | VarChar | 1 | - | N | `N` = No<br>`B` = Interest and Fee<br>`I` = Interest Only<br>`F` = Fee Only |
| 293 | `IntrAcc` | Interest Account | nVarChar | 15 | - |  |  |
| 294 | `FeeAcc` | Fee Account | nVarChar | 15 | - |  |  |
| 295 | `CpnNo` | Campaign No. | Int | 11 | [OCPN](OCPN.md) |  |  |
| 296 | `NTSWebSite` | E-Tax Web Site | Int | 6 | [OTWS](OTWS.md) |  |  |
| 297 | `DflIBAN` | Default Bank IBAN | nVarChar | 50 | - |  |  |
| 298 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 299 | `Number` | Number | Int | 11 | - |  |  |
| 300 | `EDocExpFrm` | Electronic Doc. Export Format | Int | 11 | - |  |  |
| 301 | `TaxIdIdent` | Tax ID Category | VarChar | 1 | - | 3 | `1` = Self-Employed<br>`2` = Company<br>`3` = Registered Business<br>`5` = International Company |
| 302 | `Attachment` | Attachment | Text | 16 | - |  |  |
| 303 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 304 | `DiscRel` | Disc. Relations | VarChar | 1 | - | L | `L` = Lowest Discount<br>`H` = Highest Discount<br>`A` = Average<br>`S` = Total<br>`M` = Discount Multiples |
| 305 | `NoDiscount` | No Discounts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 306 | `SCAdjust` | SC Adjustment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 307 | `DflAgrmnt` | Default Blanket Agreement No. | Int | 11 | [OOAT](OOAT.md) |  |  |
| 308 | `GlblLocNum` | Global Location Number | nVarChar | 50 | - |  |  |
| 309 | `SenderID` | EDI Message Sender ID | nVarChar | 50 | - |  |  |
| 310 | `RcpntID` | EDI Message Recipient ID | nVarChar | 50 | - |  |  |
| 311 | `MainUsage` | Main Usage | Int | 11 | - |  |  |
| 312 | `SefazCheck` | Check BP Status on SEFAZ | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 313 | `ChecksBalL` | Open Checks Balance in LC | Num | 19.6 | - |  |  |
| 314 | `ChecksBalS` | Open Checks Balance in SC | Num | 19.6 | - |  |  |
| 315 | `DateFrom` | Relationship Initial Date | Date | 8 | - |  |  |
| 316 | `DateTill` | Relationship Final Date | Date | 8 | - |  |  |
| 317 | `RelCode` | Relationship Code | nVarChar | 2 | - |  | `01` = Matriz no exterior<br>`02` = Filial, inclusive ag�ncia ou depend�ncia, no exterior<br>`03` = Coligada, inclusive equiparada<br>`04` = Controladora<br>`05` = Controlada (exceto subsidi�ria integral)<br>`06` = Subsidi�ria integral<br>`07` = Controlada em conjunto<br>`08` = Entidade de Prop�sito Espec�fico (conforme defini��o da CVM)<br>`09` = Participante do conglomerado, conforme norma espec�fica do �rg�o regulador, exceto as que se enquadrem nos tipos precedentes<br>`10` = Vinculadas (Art. 23 da Lei 9.430/96), exceto as que se enquadrem nos tipos precedentes<br>`11` = Localizada em pa�s com tributa��o favorecida (Art. 24 da Lei 9.430/96), exceto as que se enquadrem nos tipos precedentes |
| 318 | `OKATO` | OKATO | nVarChar | 11 | - |  |  |
| 319 | `OKTMO` | OKTMO | nVarChar | 12 | - |  |  |
| 320 | `KBKCode` | KBK Budget Classification Code | nVarChar | 20 | - |  |  |
| 321 | `TypeOfOp` | Type of Operation | VarChar | 1 | - | O | `P` = Professional Services<br>`R` = Renting Assets<br>`O` = Others<br>`D` = Disposal of Goods<br>`S` = Import of Goods and Services<br>`V` = Import by Virtual Transfer<br>`G` = Global Operations |
| 322 | `OwnerCode` | BP Owner | Int | 11 | [OHEM](OHEM.md) |  |  |
| 323 | `MandateID` | Mandate ID | nVarChar | 35 | - |  |  |
| 324 | `SignDate` | Date of Signature | Date | 8 | - |  |  |
| 325 | `Remark1` | Remark 1 | Int | 11 | [ORMK](ORMK.md) |  |  |
| 326 | `ConCerti` | Concessional Certificate | nVarChar | 20 | - |  |  |
| 327 | `TpCusPres` | Type of End-User Presence | Int | 11 | [OBNI](OBNI.md) | 9 |  |
| 328 | `RoleTypCod` | Role Type Code | nVarChar | 2 | - |  |  |
| 329 | `BlockComm` | Block Sending Marketing | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 330 | `EmplymntCt` | Employment Category | nVarChar | 3 | [OETC](OETC.md) |  |  |
| 331 | `ExcptnlEvt` | Exceptional Event | nVarChar | 2 | [OEPE](OEPE.md) |  |  |
| 332 | `ExpnPrfFnd` | Professional Funds Expenses | Num | 19.6 | - |  |  |
| 333 | `EdrsFromBP` | Endorsable Checks from This BP | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 334 | `EdrsToBP` | This BP Accepts Endorsed Checks | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 335 | `CreateTS` | Creatn Time - Incl. Secs | Int | 11 | - |  |  |
| 336 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 337 | `EDocGenTyp` | Electr. Doc. Generation Type | VarChar | 1 | - |  | `N` = Not Relevant<br>`G` = Generate<br>`L` = Generate - Later<br>`S` = Send<br>`R` = Send - Later |
| 338 | `eStreet` | Street | nVarChar | 38 | - |  |  |
| 339 | `eStreetNum` | Street Number | nVarChar | 4 | - |  |  |
| 340 | `eBuildnNum` | Building Number | Int | 11 | - |  |  |
| 341 | `eZipCode` | Zip Code | nVarChar | 10 | - |  |  |
| 342 | `eCityTown` | City/Town/Village | nVarChar | 48 | - |  |  |
| 343 | `eCountry` | Country | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 344 | `eDistrict` | District | nVarChar | 3 | - |  |  |
| 345 | `RepFName` | Representative First Name | nVarChar | 20 | - |  |  |
| 346 | `RepSName` | Representative Surname | nVarChar | 36 | - |  |  |
| 347 | `RepCmpName` | Company Name | nVarChar | 36 | - |  |  |
| 348 | `RepFisCode` | Representative Fiscal Code | nVarChar | 16 | - |  |  |
| 349 | `RepAddID` | Representative Additional ID | nVarChar | 28 | - |  |  |
| 350 | `PECAddr` | PEC Address | nVarChar | 254 | - |  |  |
| 351 | `IPACodePA` | Receiver Code for Public Administration | nVarChar | 32 | - |  |  |
| 352 | `PriceMode` | Price Mode | VarChar | 1 | - |  | `N` = Net<br>`G` = Gross |
| 353 | `EffecPrice` | Effective Price | VarChar | 1 | - | D | `D` = Default Priority<br>`L` = Lowest Price<br>`H` = Highest Price |
| 354 | `TxExMxVdTp` | Exemption Max validate type | VarChar | 1 | - | I | `I` = Apply to Individual Documents<br>`A` = Apply to Accumulated Document Amount |
| 355 | `MerchantID` | Merchant ID | nVarChar | 15 | - |  |  |
| 356 | `UseBilAddr` | Determine GST by Using Bill to | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 357 | `NaturalPer` | Natural Person | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 358 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased<br>`B` = Blocked<br>`U` = Unblocked |
| 359 | `EnAddID` | Encryption of ID No. 2 | Text | 16 | - |  |  |
| 360 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 361 | `EnDflAccnt` | Encryption of Default Account | Text | 16 | - |  |  |
| 362 | `EnDflIBAN` | Encryption of Default IBAN | Text | 16 | - |  |  |
| 363 | `EnERD4In` | Enable ERD for Incoming Payments | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 364 | `EnERD4Out` | Enable ERD for Outgoing Payments | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 365 | `DflCustomr` | Default Customer | VarChar | 1 | - | N | `N` = Not a default customer<br>`D` = Default Customer<br>`P` = Partially erased<br>`C` = Default customer who has been partially erased |
| 366 | `TspEntry` | Default Transporter | Int | 11 | [OTSP](OTSP.md) |  |  |
| 367 | `TspLine` | Default Transportation Line | Int | 11 | - |  |  |
| 368 | `FCERelevnt` | FCE Relevant | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 369 | `FCEVldte` | FCE Validate Base Delivery | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 370 | `AggregDoc` | Aggregate Document | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 371 | `EffcAllSrc` | Considers All Price Sources | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 372 | `EBVatExCau` | VAT Exemption Cause | Int | 11 | [OVEC](OVEC.md) |  |  |
| 373 | `DataVers` | Data Version | Int | 11 | - | 1 |  |
| 374 | `LegalText` | Legal Text | nVarChar | 254 | - |  |  |
| 375 | `VatResDate` | VAT Verfication Response Date | Date | 8 | - |  |  |
| 376 | `VatResCode` | VAT Verfication Response Code | Int | 11 | [ORVC](ORVC.md) |  |  |
| 377 | `EnIBAN` | Encryption of IBAN | Text | 16 | - |  |  |
| 378 | `DefaultCur` | Default Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 379 | `VatResName` | VAT Verfication Response Name | nVarChar | 254 | - |  |  |
| 380 | `VatResAddr` | VAT Verfication Response Addr | nVarChar | 254 | - |  |  |
| 381 | `CertDetail` | Certificate Details | nVarChar | 100 | - |  |  |
| 382 | `EORINumber` | EORI Number | nVarChar | 17 | - |  |  |
| 383 | `FCEPmnMean` | Use FCEs as Payment Means | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 384 | `DefCommDDt` | Defer Commitment Limit on Due Date | VarChar | 1 | - |  | `E` = Month End<br>`H` = Half Month<br>`S` = Month Start |
| 385 | `DefCommMon` | Defer Commitment Limit on Due Date - Months | Int | 6 | - |  |  |
| 386 | `DefCommDay` | Defer Commitment Limit on Due Date - Days | Int | 6 | - |  |  |
| 387 | `ExLettDate` | Exemption Letter Registration Date | Date | 8 | - |  |  |
| 388 | `NotRel4MI` | Not Relevant for Monthly Invoice | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 389 | `EnHBnkAcct` | Encryption of House Bank Account | Text | 16 | - |  |  |
| 390 | `EnVatIDNum` | Encrypt VAT ID Number | Text | 16 | - |  |  |
| 391 | `EnLicTradN` | Encrypt TAX ID Number | Text | 16 | - |  |  |
| 392 | `SirenNo` | SIREN No. | nVarChar | 9 | - |  |  |
| 393 | `SiretNo` | SIRET No. | nVarChar | 32 | - |  |  |
| 394 | `VATEX` | VAT Exemption Reason | nVarChar | 32 | - |  |  |
| 395 | `RoutingCod` | Routing Code | nVarChar | 100 | - |  |  |
| 396 | `PubDirStat` | Public Directory Status | nVarChar | 2 | - |  | `AP` = Active Private Entity<br>`AU` = Active Public Entity<br>`IP` = Inactive Private Entity<br>`IU` = Inactive Public Entity<br>`NR` = Not Registered |

## Claves e índices (11)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode |
| CARD_NAME | No | CardName |
| CARD_TYPE | No | CardType |
| FATHER | No | FatherCard |
| TERMS | No | GroupNum |
| CURRENCY | No | Currency |
| COM_GROUP | No | CommGrCode |
| PRICE_LIST | No | ListNum |
| PAY_ACCT | No | DebPayAcct |
| ABS_ENTRY | Yes | DocEntry |
| OWNER_CODE | No | OwnerCode |
