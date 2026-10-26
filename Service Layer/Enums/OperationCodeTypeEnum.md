# OperationCodeTypeEnum — Tipo de código de operación (España)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `OperationCodeTypeEnum`
- **Descripción (ES):** Tipo de código de operación (España)
- **Underlying type:** Edm.Int32
- **Members:** 19

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `octSummaryInvoicesEntry` | 0 | Summary Invoices Entry | Asiento resumen de facturas |
| `octSummaryReceiptsEntry` | 1 | Summary Receipts Entry | Asiento resumen de tiques |
| `octInvoicewithSeveralVATRates` | 2 | Invoicewith Several VAT Rates | Factura con varios tipos de IVA |
| `octCorrectionInvoice` | 3 | Correction Invoice | Factura rectificativa |
| `octDueVATPendingInvoiceIssuance` | 4 | Due VAT Pending Invoice Issuance | IVA devengado pendiente de emitir factura |
| `octExpensesIncurredbyTravelAgentforCustomers` | 5 | Expenses Incurredby Travel Agentfor Customers | Gastos de agencias de viaje por cuenta de clientes |
| `octSpecialRegulationforVATGroup` | 6 | Special Regulationfor VAT Group | Régimen especial de grupo de IVA |
| `octSpecialRegulationforGoldInvestment` | 7 | Special Regulationfor Gold Investment | Régimen especial del oro de inversión |
| `octReverseChargeProcedure` | 8 | Reverse Charge Procedure | Inversión del sujeto pasivo |
| `octUnsummarizedReceipts` | 9 | Unsummarized Receipts | Tiques no resumidos |
| `octIdentificationofErrorTransactions` | 10 | Identificationof Error Transactions | Identificación de operaciones con error |
| `octTransactionswithEntrepreneursIssuingReceiptsforAgriculturalCompensation` | 11 | Transactionswith Entrepreneurs Issuing Receiptsfor Agricultural Compensation | Operaciones con empresarios del régimen de compensación agraria |
| `octServiceInvoicingbyTravelAgenciesonBehalfofThirdParties` | 12 | Service Invoicingby Travel Agencieson Behalfof Third Parties | Facturación de agencias de viaje por cuenta de terceros |
| `octBusinessOfficeRental` | 13 | Business Office Rental | Arrendamiento de local de negocio |
| `octSubsidies` | 14 | Subsidies | Subvenciones |
| `octIncomingPaymentsforIndustrialandIntellectualPropertyRights` | 15 | Incoming Paymentsfor Industrialand Intellectual Property Rights | Cobros por derechos de propiedad industrial e intelectual |
| `octInsuranceTransactions` | 16 | Insurance Transactions | Operaciones de seguros |
| `octPurchasesfromTravelAgencies` | 17 | Purchasesfrom Travel Agencies | Compras a agencias de viaje |
| `octTransactionsSubjecttoProductionServiceandImportTaxesinCeutaandMelilla` | 18 | Transactions Subjectto Production Serviceand Import Taxesin Ceutaand Melilla | Operaciones sujetas al IPSI de Ceuta y Melilla |

## Used by (1 properties)

- [JournalEntry](../Entidades/JournalEntries.md).`OperationCode`
