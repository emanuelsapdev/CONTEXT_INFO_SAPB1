# WTQ4 - Inventory Transfer Request - Tax Amount per Document

- **Tabla:** WTQ4
- **Descripción:** Inventory Transfer Request - Tax Amount per Document
- **Cantidad de campos:** 61
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WTQ4.html

## Campos (61)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Document ID | Int | 11 | [OWTQ](OWTQ.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - | -1 |  |
| 3 | `GroupNum` | Group No. | Int | 11 | - | -1 |  |
| 4 | `ExpnsCode` | Expense Code | Int | 11 | [OEXD](OEXD.md) | -1 |  |
| 5 | `RelateType` | Relation Type | Int | 11 | - | 1 | `1` = Row<br>`2` = Row Freight Charges<br>`3` = Document Expenses<br>`13` = Distributed Freights |
| 6 | `StcCode` | Tax Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 7 | `StaCode` | Tax Code | nVarChar | 8 | [OSTA](OSTA.md) |  |  |
| 8 | `staType` | Authority Type | Int | 11 | [OSTT](OSTT.md) |  |  |
| 9 | `TaxRate` | Authority Type | Num | 19.6 | [OSTT](OSTT.md) |  |  |
| 10 | `TaxAcct` | Authority Code | nVarChar | 15 | - |  |  |
| 11 | `TaxSum` | Tax % | Num | 19.6 | [OACT](OACT.md) |  |  |
| 12 | `TaxSumFrgn` | Tax Account | Num | 19.6 | - |  |  |
| 13 | `TaxSumSys` | Tax Amount | Num | 19.6 | - |  |  |
| 14 | `BaseSum` | Tax Amount (FC) | Num | 19.6 | - |  |  |
| 15 | `BaseSumFrg` | Base Amount | Num | 19.6 | - |  |  |
| 16 | `BaseSumSys` | Base Amount (FC) | Num | 19.6 | - |  |  |
| 17 | `ObjectType` | Base Amount (SC) | nVarChar | 20 | - |  |  |
| 18 | `LogInstanc` | Tax Amount (SC) | Int | 11 | [ADP1](ADP1.md) | 0 |  |
| 19 | `TaxStatus` | Base Amount | VarChar | 1 | - | Y | `Y` = Regular Tax<br>`N` = No Tax<br>`U` = Use Tax |
| 20 | `VatApplied` | VAT Applied | Num | 19.6 | - |  |  |
| 21 | `VatAppldFC` | Applied Tax (FC) | Num | 19.6 | - |  |  |
| 22 | `VatAppldSC` | Applied Tax (SC) | Num | 19.6 | - |  |  |
| 23 | `LineSeq` | Line Sequence | Int | 11 | - |  |  |
| 24 | `DeferrAcct` | Deferred Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 25 | `BaseType` | Base Document Type | Int | 11 | - | -1 |  |
| 26 | `BaseAbs` | Base Doc Abs Entry | Int | 11 | - | -1 |  |
| 27 | `BaseSeq` | Base Doc. Line Sequence | Int | 11 | - |  |  |
| 28 | `DeductTax` | Deductible Tax Amount | Num | 19.6 | - |  |  |
| 29 | `DdctTaxFrg` | Deductible Tax Amount (FC) | Num | 19.6 | - |  |  |
| 30 | `DdctTaxSys` | Deductible Tax Amount (SC) | Num | 19.6 | - |  |  |
| 31 | `BaseAppld` | Applied Base Amount | Num | 19.6 | - |  |  |
| 32 | `BaseApldFC` | Applied Base Amount (FC) | Num | 19.6 | - |  |  |
| 33 | `BaseApldSC` | Applied Base Amount (SC) | Num | 19.6 | - |  |  |
| 34 | `NonDdctPrc` | Non Deductible % | Num | 19.6 | - |  |  |
| 35 | `NonDdctAct` | Non Deductible Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 36 | `TaxInPrice` | Tax Included in Price? | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 37 | `Exempt` | Exempt? | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 38 | `TaxExpAct` | Expense Account for Tax | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 39 | `OnHoldTax` | On Hold Tax Amount | Num | 19.6 | - |  |  |
| 40 | `OnHoldTaxF` | On Hold Tax Amount (FC) | Num | 19.6 | - |  |  |
| 41 | `OnHoldTaxS` | On Hold Tax Amount (SC) | Num | 19.6 | - |  |  |
| 42 | `InGrossRev` | Included in Gross Revenue | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 43 | `TaxSumOrg` | Tax Amount Original | Num | 19.6 | - |  |  |
| 44 | `TaxSumOrgF` | Tax Amount Original (FC) | Num | 19.6 | - |  |  |
| 45 | `TaxSumOrgS` | Tax Amount Original (SC) | Num | 19.6 | - |  |  |
| 46 | `OpenTax` | Open Service Tax | Num | 19.6 | - |  |  |
| 47 | `OpenTaxFC` | Open Service Tax (FC) | Num | 19.6 | - |  |  |
| 48 | `OpenTaxSC` | Open Service Tax (SC) | Num | 19.6 | - |  |  |
| 49 | `Unencumbrd` | Unencumbered | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 50 | `TaxOnRI` | Tax On Reserve Invoice | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 51 | `RvsChrgPrc` | Reverse Charge % | Num | 19.6 | - |  |  |
| 52 | `RvsChrgTax` | Reverse Charge Tax Amount | Num | 19.6 | - |  |  |
| 53 | `RvsChrgSC` | Reverse Charge Tax Amount (SC) | Num | 19.6 | - |  |  |
| 54 | `RvsChrgFC` | Reverse Charge Tax Amount (FC) | Num | 19.6 | - |  |  |
| 55 | `InFirstIns` | Included in First Installment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 56 | `ExtTaxRate` | External Tax Rate | Num | 19.6 | - |  |  |
| 57 | `ExtTaxSum` | External Tax Amount | Num | 19.6 | - |  |  |
| 58 | `TaxAmtSrc` | Tax Amount Source | VarChar | 1 | - | S | `S` = Internal System Calculation<br>`E` = External Calculation |
| 59 | `ExtTaxSumF` | External Tax Amount (FC) | Num | 19.6 | - |  |  |
| 60 | `ExtTaxSumS` | External Tax Amount (SC) | Num | 19.6 | - |  |  |
| 61 | `CESTrel` | CEST Relevant | VarChar | 1 | - | N | `Y`<br>`N` |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineSeq, ObjectType, LogInstanc |
| SCONDARY | No | DocEntry, LineNum, GroupNum, ExpnsCode, StcCode, StaCode, staType |
