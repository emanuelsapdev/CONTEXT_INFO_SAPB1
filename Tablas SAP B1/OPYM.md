# OPYM - Payment Methods for Payment Wizard

- **Tabla:** OPYM
- **Descripción:** Payment Methods for Payment Wizard
- **Cantidad de campos:** 65
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPYM.html

## Campos (65)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PayMethCod` | Payment Method Code | nVarChar | 15 | - |  |  |
| 2 | `Descript` | Description | nVarChar | 100 | - |  |  |
| 3 | `Type` | Type | VarChar | 1 | - |  | `O` = Outgoing<br>`I` = Incoming |
| 4 | `BankTransf` | Payment Means | VarChar | 1 | - |  | `C` = Check<br>`T` = Bank Transfer<br>`B` = Bill of Exchange |
| 5 | `Address` | Check Address | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `BankDet` | Check Bank Details | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `CllctAutor` | Check Collection Authorization | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `FrgnPmntBl` | Block Foreign Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `FrgnBnkBl` | Block Foreign Bank | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `CurrRestr` | Currency Restriction | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `PostOffBnk` | Post Office Bank | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `MinAmount` | Minimum Amount | Num | 19.6 | - |  |  |
| 13 | `MaxAmount` | Maximum Amount | Num | 19.6 | - |  |  |
| 14 | `BnkDflt` | Default Bank | nVarChar | 30 | - |  |  |
| 15 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 16 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 17 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 18 | `BankCountr` | Bank Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 19 | `DflAccount` | Default Bank Account | nVarChar | 50 | - |  |  |
| 20 | `GLAccount` | G/L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 21 | `Branch` | Bank Branch | nVarChar | 50 | - |  |  |
| 22 | `KeyCode` | Key Code | nVarChar | 6 | - |  |  |
| 23 | `TrnsType` | Transaction Type | nVarChar | 2 | - |  |  |
| 24 | `Format` | File Format | nVarChar | 11 | [OFRM](OFRM.md) |  |  |
| 25 | `AgtCollect` | Agent Collection | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 26 | `SendAccept` | Send for Acceptance | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 27 | `GrpByDate` | Group By Date | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 28 | `DepNorm` | Deposit Norm | nVarChar | 8 | - |  |  |
| 29 | `DebitMemo` | Debit Memo | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 30 | `GroupPmRef` | Group by Payment Reference No. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 31 | `GroupInv` | Group Invoices by Pay | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 32 | `ValDateSel` | Due Date Selection | VarChar | 1 | - | P | `P` = Date of Payment Run<br>`I` = Due Date of Invoice<br>`T` = Payment Terms |
| 33 | `PaymTerms` | Payment Terms Code | Int | 6 | [OCTG](OCTG.md) |  |  |
| 34 | `IntrimAcct` | Post to G/L Interim Account | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 35 | `BnkActKey` | Bank Account Key | Int | 11 | [DSC1](DSC1.md) |  |  |
| 36 | `DocType` | BoE Document Type | nVarChar | 2 | - |  |  |
| 37 | `Accepted` | BoE Status - Accepted | VarChar | 1 | - |  |  |
| 38 | `PtfID` | BoE Internal Portfolio ID | nVarChar | 3 | - |  |  |
| 39 | `PtfCode` | BoE Portfolio Code | nVarChar | 2 | - |  |  |
| 40 | `PtfNum` | BoE Portfolio Number | nVarChar | 4 | - |  |  |
| 41 | `CurCode` | BoE Currency Code | nVarChar | 2 | - |  |  |
| 42 | `Instruct1` | BoE Instruction 1 | nVarChar | 2 | - |  |  |
| 43 | `Instruct2` | BoE Instruction 2 | nVarChar | 2 | - |  |  |
| 44 | `PaymntPlc` | BoE Payment Place | nVarChar | 128 | - |  |  |
| 45 | `BoeDll` | Bar Code DLL | nVarChar | 50 | - |  |  |
| 46 | `BankCtlKey` | Bank Control No. | nVarChar | 2 | - |  |  |
| 47 | `Active` | Status of the Payment Method | VarChar | 1 | - | Y | `Y` = Active<br>`N` = Inactive |
| 48 | `BcgPcnt` | Bank Charge Rate (%) | Num | 19.6 | - |  |  |
| 49 | `GrpByCur` | Group Invoices by Currency | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 50 | `GrpByBank` | Group Invoices by Pay-To Bank | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 51 | `DflIBAN` | Bank IBAN | nVarChar | 50 | - |  |  |
| 52 | `DflSwift` | Bank BIC/SWIFT | nVarChar | 50 | - |  |  |
| 53 | `BoeReport` | BoE Report Code | nVarChar | 8 | - |  |  |
| 54 | `CancInstr` | Cancellation Instruction | nVarChar | 2 | - |  |  |
| 55 | `OccurCode` | Occurrence Code | nVarChar | 2 | - |  |  |
| 56 | `MovmntCode` | Movement Code | nVarChar | 10 | - |  |  |
| 57 | `NegPymCode` | Negative Payment Method Code | nVarChar | 15 | [OPYM](OPYM.md) |  |  |
| 58 | `DirectDbt` | Direct Debit | nVarChar | 5 | - |  | `CORE`<br>`B2B`<br>`COR1` |
| 59 | `IssueIndic` | Issue Indicator | VarChar | 1 | - | R | `3`<br>`R` |
| 60 | `PrintSEPA` | Print SEPA Prenotification | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 61 | `PmntType` | Payment Type | nVarChar | 50 | - | 01 | `01` = Efectivo<br>`02` = Cheque nominativo<br>`03` = Transferencia electr�nica de fondos<br>`04` = Tarjeta de cr�dito<br>`05` = Monedero electr�nico<br>`06` = Dinero electr�nico<br>`08` = Vales de despensa<br>`12` = Daci�n en pago<br>`13` = Pago por subrogaci�n<br>`14` = Pago por consignaci�n<br>`15` = Condonaci�n<br>`17` = Compensaci�n<br>`23` = Novaci�n<br>`24` = Confusi�n<br>`25` = Remisi�n de deuda<br>`26` = Prescripci�n o caducidad<br>`27` = A satisfacci�n del acreedor<br>`28` = Tarjeta de d�bito<br>`29` = Tarjeta de servicios<br>`30` = Aplicaci�n de anticipos<br>`31` = Intermediario pagos<br>`99` = Por definir |
| 62 | `GrpByAgrNo` | Group Blanket Agreement | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 63 | `SpltPmtVAT` | Split Payments for VAT | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 64 | `EnDflAcct` | Encryption of Default Bank Account | Text | 16 | - |  |  |
| 65 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PayMethCod |
