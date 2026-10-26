# JournalEntryLine — Líneas del asiento contable

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `JournalEntryLine`
- **Descripción (ES):** Líneas del asiento contable
- **Description (EN):** Journal Entry Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 66

## Properties (66)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Line_ID` | Edm.Int32 | Yes | Line ID | ID de línea |
| 2 | `AccountCode` | Edm.String | Yes | Account Code | Código de cuenta |
| 3 | `Debit` | Edm.Double | Yes | Debit | Debe/Débito |
| 4 | `Credit` | Edm.Double | Yes | Credit | Haber/Crédito |
| 5 | `FCDebit` | Edm.Double | Yes | FC (foreign currency) Debit | Debe (ME) |
| 6 | `FCCredit` | Edm.Double | Yes | FC (foreign currency) Credit | Haber (ME) |
| 7 | `FCCurrency` | Edm.String | Yes | FC (foreign currency) Currency | Moneda extranjera |
| 8 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 9 | `ShortName` | Edm.String | Yes | Short Name | Nombre corto |
| 10 | `ContraAccount` | Edm.String | Yes | Contra Account | Contracuenta |
| 11 | `LineMemo` | Edm.String | Yes | Line Memo | Comentario de línea |
| 12 | `ReferenceDate1` | Edm.DateTimeOffset | Yes | Reference Date 1 | Fecha de referencia 1 |
| 13 | `ReferenceDate2` | Edm.DateTimeOffset | Yes | Reference Date 2 | Fecha de referencia 2 |
| 14 | `Reference1` | Edm.String | Yes | Reference 1 | Referencia 1 |
| 15 | `Reference2` | Edm.String | Yes | Reference 2 | Referencia 2 |
| 16 | `ProjectCode` | Edm.String | Yes | Project Code | Código de proyecto |
| 17 | `CostingCode` | Edm.String | Yes | Costing Code | Norma de reparto (dimensión 1) |
| 18 | `TaxDate` | Edm.DateTimeOffset | Yes | Tax Date | Fecha del documento (fecha de impuestos) |
| 19 | `BaseSum` | Edm.Double | Yes | Base Sum | Importe base |
| 20 | `TaxGroup` | Edm.String | Yes | Tax Group | Grupo de impuestos |
| 21 | `DebitSys` | Edm.Double | Yes | Debit (system currency) | Debe (moneda del sistema) |
| 22 | `CreditSys` | Edm.Double | Yes | Credit (system currency) | Haber (moneda del sistema) |
| 23 | `VatDate` | Edm.DateTimeOffset | Yes | Vat Date | Fecha de IVA |
| 24 | `VatLine` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Vat Line | Línea de IVA |
| 25 | `SystemBaseAmount` | Edm.Double | Yes | System Base Amount | Importe base (moneda del sistema) |
| 26 | `VatAmount` | Edm.Double | Yes | Vat Amount | Importe de IVA |
| 27 | `SystemVatAmount` | Edm.Double | Yes | System Vat Amount | Importe de IVA (moneda del sistema) |
| 28 | `GrossValue` | Edm.Double | Yes | Gross Value | Valor bruto |
| 29 | `AdditionalReference` | Edm.String | Yes | Additional Reference | Referencia adicional |
| 30 | `CheckAbs` | Edm.Int32 | Yes | Check Abs | Entrada del cheque |
| 31 | `CostingCode2` | Edm.String | Yes | Costing Code 2 | Norma de reparto (dimensión 2) |
| 32 | `CostingCode3` | Edm.String | Yes | Costing Code 3 | Norma de reparto (dimensión 3) |
| 33 | `CostingCode4` | Edm.String | Yes | Costing Code 4 | Norma de reparto (dimensión 4) |
| 34 | `TaxCode` | Edm.String | Yes | Tax Code | Indicador de impuesto |
| 35 | `TaxPostAccount` | [BoTaxPostAccEnum](../Enums/BoTaxPostAccEnum.md) | Yes | Tax Post Account | Cuenta de contabilización de impuestos |
| 36 | `CostingCode5` | Edm.String | Yes | Costing Code 5 | Norma de reparto (dimensión 5) |
| 37 | `LocationCode` | Edm.Int32 | Yes | Location Code | Código de ubicación |
| 38 | `ControlAccount` | Edm.String | Yes | Control Account | Cuenta asociada |
| 39 | `EqualizationTaxAmount` | Edm.Double | Yes | Equalization Tax Amount | Importe de recargo de equivalencia |
| 40 | `SystemEqualizationTaxAmount` | Edm.Double | Yes | System Equalization Tax Amount | Recargo de equivalencia (moneda del sistema) |
| 41 | `TotalTax` | Edm.Double | Yes | Total Tax | Impuesto total |
| 42 | `SystemTotalTax` | Edm.Double | Yes | System Total Tax | Impuesto total (moneda del sistema) |
| 43 | `WTLiable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Withholding Tax Liable | Sujeto a retención |
| 44 | `WTRow` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Withholding Tax Row | Línea de retención |
| 45 | `PaymentBlock` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Payment Block | Bloqueo de pago |
| 46 | `BlockReason` | Edm.Int32 | Yes | Block Reason | Motivo del bloqueo |
| 47 | `FederalTaxID` | Edm.String | Yes | Federal Tax ID | CUIT / ID fiscal federal |
| 48 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |
| 49 | `BPLName` | Edm.String | Yes | Branch Name | Nombre de la sucursal |
| 50 | `VATRegNum` | Edm.String | Yes | VAT Reg Number | Número de registro de IVA |
| 51 | `PaymentOrdered` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Payment Ordered | Pago ordenado |
| 52 | `ExposedTransNumber` | Edm.Int32 | Yes | Exposed Trans Number | Número de transacción expuesto |
| 53 | `DocumentArray` | Edm.Int32 | Yes | Document Array | Matriz de documentos |
| 54 | `DocumentLine` | Edm.Int32 | Yes | Document Line | Línea del documento |
| 55 | `CostElementCode` | Edm.String | Yes | Cost Element Code | Código de elemento de costo |
| 56 | `Cig` | Edm.Int32 | Yes | Cig | Código CIG |
| 57 | `Cup` | Edm.Int32 | Yes | Cup | Código CUP |
| 58 | `IncomeClassificationCategory` | Edm.Int32 | Yes | Income Classification Category | Categoría de clasificación de ingresos |
| 59 | `IncomeClassificationType` | Edm.Int32 | Yes | Income Classification Type | Tipo de clasificación de ingresos |
| 60 | `ExpensesClassificationCategory` | Edm.Int32 | Yes | Expenses Classification Category | Categoría de clasificación de gastos |
| 61 | `ExpensesClassificationType` | Edm.Int32 | Yes | Expenses Classification Type | Tipo de clasificación de gastos |
| 62 | `VATClassificationCategory` | Edm.Int32 | Yes | VAT Classification Category | Categoría de clasificación de IVA |
| 63 | `VATClassificationType` | Edm.Int32 | Yes | VAT Classification Type | Tipo de clasificación de IVA |
| 64 | `VATExemptionCause` | Edm.Int32 | Yes | VAT Exemption Cause | Causa de exención de IVA |
| 65 | `LineAllocationNumber` | Edm.String | Yes | Line Allocation Number | Número de asignación de línea |
| 66 | `CashFlowAssignments` | Collection([CashFlowAssignment](../Tipos-Complejos/CashFlowAssignment.md)) | Yes | Cash Flow Assignments | Asignaciones de flujo de caja |

## Used by (properties)

- [JournalEntry](../Entidades/JournalEntries.md).`JournalEntryLines`
