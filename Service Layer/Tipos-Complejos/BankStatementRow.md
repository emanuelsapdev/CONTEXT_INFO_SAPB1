# BankStatementRow — Líneas del extracto bancario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BankStatementRow`
- **Descripción (ES):** Líneas del extracto bancario
- **Description (EN):** Bank Statement Row
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 51

## Properties (51)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ExternalBankStatementNo` | Edm.Int32 | Yes | External Bank Statement Number | Número de extracto bancario externo |
| 2 | `AccountNumber` | Edm.String | Yes | Account Number | Número de cuenta |
| 3 | `SequenceNo` | Edm.Int32 | Yes | Sequence Number | Número de secuencia |
| 4 | `AccountName` | Edm.String | Yes | Account Name | Nombre de cuenta |
| 5 | `Reference` | Edm.String | Yes | Reference | Referencia |
| 6 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 7 | `Details` | Edm.String | Yes | Details | Detalles |
| 8 | `DebitAmountFC` | Edm.Double | Yes | Debit Amount FC (foreign currency) | Importe del debe (ME) |
| 9 | `CreditAmountFC` | Edm.Double | Yes | Credit Amount FC (foreign currency) | Importe del haber (ME) |
| 10 | `CreditCurrency` | Edm.String | Yes | Credit Currency | Moneda del crédito |
| 11 | `Balance` | Edm.Double | Yes | Balance | Saldo |
| 12 | `ReconciliationNo` | Edm.Int32 | Yes | Reconciliation Number | Número de conciliación |
| 13 | `ExternalCode` | Edm.String | Yes | External Code | Código externo |
| 14 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 15 | `BPName` | Edm.String | Yes | Business Partner Name | Nombre del socio de negocios |
| 16 | `StatementNumber` | Edm.Int32 | Yes | Statement Number | Número del extracto |
| 17 | `RowStatus` | Edm.String | Yes | Row Status | Estado de línea |
| 18 | `VisualOrder` | Edm.Int32 | Yes | Visual Order | Orden visual |
| 19 | `DocNumType` | [BoBpsDocTypes](../Enums/BoBpsDocTypes.md) | Yes | Document Number Type | Tipo de número de documento |
| 20 | `Details2` | Edm.String | Yes | Details 2 | Detalles 2 |
| 21 | `PaymentReferenceNo` | Edm.String | Yes | Payment Reference Number | N.º de referencia del pago |
| 22 | `CreateMethod` | [CreateMethodEnum](../Enums/CreateMethodEnum.md) | Yes | Create Method | Método de creación |
| 23 | `BankStmtLineDate` | Edm.DateTimeOffset | Yes | Bank Stmt Line Date | Fecha de línea del extracto bancario |
| 24 | `BankStmtDueDate` | Edm.DateTimeOffset | Yes | Bank Stmt Due Date | Fecha de vencimiento del extracto bancario |
| 25 | `InternalBankOpCode` | Edm.Int32 | Yes | Internal Bank Op Code | Código de operación bancaria interna |
| 26 | `BPBankAccount` | Edm.String | Yes | Business Partner Bank Account | Cuenta bancaria del socio de negocios |
| 27 | `DebitAmountLC` | Edm.Double | Yes | Debit Amount LC (local currency) | Importe del debe (moneda local) |
| 28 | `CreditAmountLC` | Edm.Double | Yes | Credit Amount LC (local currency) | Importe del haber (moneda local) |
| 29 | `ExchangeRate` | Edm.Double | Yes | Exchange Rate | Tipo de cambio |
| 30 | `IBANofBPBankAccount` | Edm.String | Yes | IBA Nof Business Partner Bank Account | IBAN de la cuenta bancaria del socio de negocios |
| 31 | `FeeOnTheLine` | Edm.Double | Yes | Fee On The Line | Cargo en la línea |
| 32 | `VATAmountLC` | Edm.Double | Yes | VAT Amount LC (local currency) | Importe de IVA (moneda local) |
| 33 | `VATAmountFC` | Edm.Double | Yes | VAT Amount FC (foreign currency) | Importe de IVA (ME) |
| 34 | `JournalEntryID` | Edm.Int32 | Yes | Journal Entry ID | ID de asiento contable |
| 35 | `PaymentID` | Edm.Int32 | Yes | Payment ID | ID del pago |
| 36 | `DocumentType` | [BankStatementDocTypeEnum](../Enums/BankStatementDocTypeEnum.md) | Yes | Document Type | Tipo de documento |
| 37 | `PostingMethod` | [PostingMethodEnum](../Enums/PostingMethodEnum.md) | Yes | Posting Method | Método de contabilización |
| 38 | `GLAccountforFee` | Edm.String | Yes | G/L Accountfor Fee | Cuenta de mayor para cargos |
| 39 | `FeeProfitCenter` | Edm.String | Yes | Fee Profit Center | Centro de beneficio de cargos |
| 40 | `FeeProject` | Edm.String | Yes | Fee Project | Proyecto de cargos |
| 41 | `BPBankCode` | Edm.String | Yes | Business Partner Bank Code | Código de banco del socio de negocios |
| 42 | `FeeDistributionRule` | Edm.String | Yes | Fee Distribution Rule | Norma de reparto de cargos |
| 43 | `FeeDistributionRule2` | Edm.String | Yes | Fee Distribution Rule 2 | Norma de reparto de cargos 2 |
| 44 | `FeeDistributionRule3` | Edm.String | Yes | Fee Distribution Rule 3 | Norma de reparto de cargos 3 |
| 45 | `FeeDistributionRule4` | Edm.String | Yes | Fee Distribution Rule 4 | Norma de reparto de cargos 4 |
| 46 | `FeeDistributionRule5` | Edm.String | Yes | Fee Distribution Rule 5 | Norma de reparto de cargos 5 |
| 47 | `BPBICSwiftCode` | Edm.String | Yes | BPBIC Swift Code | BIC/SWIFT del socio de negocios |
| 48 | `Source` | [BankStatementRowSourceEnum](../Enums/BankStatementRowSourceEnum.md) | Yes | Source | Origen |
| 49 | `FolioPrefixString` | Edm.String | Yes | Folio Prefix String | Prefijo de folio (letra) |
| 50 | `FolioNumber` | Edm.Int32 | Yes | Folio Number | Número de folio |
| 51 | `MultiplePayments` | Collection([MultiplePayment](../Tipos-Complejos/MultiplePayment.md)) | Yes | Multiple Payments | Pagos múltiples |

## Used by (properties)

- [BankStatement](../Entidades/BankStatements.md).`BankStatementRows`
