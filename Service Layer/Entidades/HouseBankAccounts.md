# HouseBankAccounts — Cuentas bancarias propias

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `HouseBankAccounts`
- **Descripción (ES):** Cuentas bancarias propias
- **Entity type:** `HouseBankAccount` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsoluteEntry` (Edm.Int32)
- **DB tables (main / lines):** [DSC1](../../Tablas%20SAP%20B1/DSC1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 62 · **Navigation properties:** 5 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/HouseBankAccounts?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/HouseBankAccounts/$count` | Contar |
| Get by key | `GET /b1s/v2/HouseBankAccounts(1)` | Obtener por clave |
| Create | `POST /b1s/v2/HouseBankAccounts` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/HouseBankAccounts(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/HouseBankAccounts(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/HouseBankAccounts(1)` (only if the B1 object allows removal) | Borrar |

## Properties (62)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BankCode` | Edm.String | Yes | Bank Code | Código del banco |
| 2 | `AccNo` | Edm.String | Yes | Account Number | Número de cuenta |
| 3 | `Branch` | Edm.String | Yes | Branch | Sucursal |
| 4 | `NextCheckNo` | Edm.Int32 | Yes | Next Check Number | Siguiente número de cheque |
| 5 | `GLAccount` | Edm.String | Yes | G/L Account | Cuenta de mayor |
| 6 | `DSC1_STREET_ALIAS` | Edm.String | Yes | DSC 1 STREET ALIAS | Alias de calle de cuenta bancaria propia |
| 7 | `Block` | Edm.String | Yes | Block | Barrio/bloque |
| 8 | `ZipCode` | Edm.String | Yes | Zip Code | Código postal |
| 9 | `City` | Edm.String | Yes | City | Ciudad |
| 10 | `County` | Edm.String | Yes | County | Condado |
| 11 | `Country` | Edm.String | Yes | Country | País |
| 12 | `State` | Edm.String | Yes | State | Estado/provincia |
| 13 | `BISR` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | BISR | BISR (Suiza) |
| 14 | `ControlKey` | Edm.String | Yes | Control Key | Clave de control |
| 15 | `UserNo1` | Edm.String | Yes | User Number 1 | N.º de usuario 1 |
| 16 | `UserNo2` | Edm.String | Yes | User Number 2 | N.º de usuario 2 |
| 17 | `UserNo3` | Edm.String | Yes | User Number 3 | N.º de usuario 3 |
| 18 | `UserNo4` | Edm.String | Yes | User Number 4 | N.º de usuario 4 |
| 19 | `IBAN` | Edm.String | Yes | IBAN | IBAN |
| 20 | `DebtofDiscountedBillofExc` | Edm.String | Yes | Debtof Discounted Billof Exc | Deuda de letras de cambio descontadas |
| 21 | `ToleranceDays` | Edm.Int32 | Yes | Tolerance Days | Días de tolerancia |
| 22 | `MinAmountofBillofExchang` | Edm.Double | Yes | Min Amountof Billof Exchang | Importe mínimo de letra de cambio |
| 23 | `MaxAmountofBillofExchan` | Edm.Double | Yes | Max Amountof Billof Exchan | Importe máximo de letra de cambio |
| 24 | `DiscountLimit` | Edm.Double | Yes | Discount Limit | Límite de descuento |
| 25 | `DaysInAdvance` | Edm.Int32 | Yes | Days In Advance | Días de anticipación |
| 26 | `BankonCollection` | Edm.String | Yes | Bankon Collection | Banco de cobranza |
| 27 | `BankonDiscounted` | Edm.String | Yes | Bankon Discounted | Banco de descuento |
| 28 | `GLInterimAccount` | Edm.String | Yes | G/L Interim Account | Cuenta transitoria de mayor |
| 29 | `AbsoluteEntry` 🔑 | Edm.Int32 | No | Absolute Entry | Entrada absoluta (ID interno) |
| 30 | `BankKey` | Edm.Int32 | Yes | Bank Key | Clave bancaria |
| 31 | `LockChecksPrinting` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Lock Checks Printing | Bloquear impresión de cheques |
| 32 | `TemplateName` | Edm.String | Yes | Template Name | Nombre de la plantilla |
| 33 | `MaximumLines` | Edm.Int32 | Yes | Maximum Lines | Líneas máximas |
| 34 | `PrintOn` | [PrintOnEnum](../Enums/PrintOnEnum.md) | Yes | Print On | Imprimir en |
| 35 | `CustomerIdNumber` | Edm.String | Yes | Customer ID Number | Número de identificación del cliente |
| 36 | `ISRBillerID` | Edm.String | Yes | ISR Biller ID | ID de facturador ISR |
| 37 | `ISRType` | Edm.Int32 | Yes | ISR Type | Tipo ISR |
| 38 | `AccountCheckDigit` | Edm.String | Yes | Account Check Digit | Dígito de control de la cuenta |
| 39 | `OurNumber` | Edm.Int32 | Yes | Our Number | Nuestro número |
| 40 | `AgreementNumber` | Edm.String | Yes | Agreement Number | Número de acuerdo |
| 41 | `AddressType` | Edm.String | Yes | Address Type | Tipo de dirección |
| 42 | `StreetNo` | Edm.String | Yes | Street Number | Número de calle |
| 43 | `Building` | Edm.String | Yes | Building | Edificio |
| 44 | `IncomingPaymentSeries` | Edm.Int32 | Yes | Incoming Payment Series | Serie de pagos recibidos |
| 45 | `OutgoingPaymentSeries` | Edm.Int32 | Yes | Outgoing Payment Series | Serie de pagos efectuados |
| 46 | `JournalEntrySeries` | Edm.Int32 | Yes | Journal Entry Series | Serie del asiento contable |
| 47 | `ImportFileName` | Edm.String | Yes | Import File Name | Nombre del archivo de importación |
| 48 | `AccountName` | Edm.String | Yes | Account Name | Nombre de cuenta |
| 49 | `BICSwiftCode` | Edm.String | Yes | BIC Swift Code | Código BIC/SWIFT |
| 50 | `FineAccount` | Edm.String | Yes | Fine Account | Cuenta de multas |
| 51 | `InterestAccount` | Edm.String | Yes | Interest Account | Cuenta de intereses |
| 52 | `DiscountAccount` | Edm.String | Yes | Discount Account | Cuenta de descuentos |
| 53 | `ServiceFeeAccount` | Edm.String | Yes | Service Fee Account | Cuenta de tarifa de servicio |
| 54 | `IOFTaxAccount` | Edm.String | Yes | IOF Tax Account | Cuenta de impuesto IOF |
| 55 | `OtherExpensesAccount` | Edm.String | Yes | Other Expenses Account | Cuenta de otros gastos |
| 56 | `OtherIncomesAccount` | Edm.String | Yes | Other Incomes Account | Cuenta de otros ingresos |
| 57 | `RetornoFileName` | Edm.String | Yes | Retorno File Name | Nombre del archivo de retorno |
| 58 | `BranchCheckDigit` | Edm.String | Yes | Branch Check Digit | Dígito de control de sucursal |
| 59 | `CollectionCode` | Edm.String | Yes | Collection Code | Código de cobranza |
| 60 | `FileSeqNextNumber` | Edm.Int32 | Yes | File Seq Next Number | Siguiente número de secuencia de archivo |
| 61 | `NoValidationForStartingEndingBal` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Number Validation For Starting Ending Bal | Sin validación de saldos inicial/final |
| 62 | `ECheck` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | E Check | Cheque electrónico |

## Navigation properties (5)

Use `GET /b1s/v2/HouseBankAccounts(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `WizardPaymentMethods` | Collection([WizardPaymentMethod](../Entidades/WizardPaymentMethods.md)) | [WizardPaymentMethods](WizardPaymentMethods.md) |  | Vías de pago del asistente de pagos |
| `BankStatements` | Collection([BankStatement](../Entidades/BankStatements.md)) | [BankStatements](BankStatements.md) |  | Extractos bancarios |
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | GLAccount → Code | Plan de cuentas (cuentas de mayor) |
| `Country2` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | Country → Code | Países/Regiones |
| `Bank` | [Bank](../Entidades/Banks.md) | [Banks](Banks.md) | BankKey → AbsoluteEntry | Banco |
