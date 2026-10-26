# PaymentDrafts — Borradores de pagos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `PaymentDrafts`
- **Descripción (ES):** Borradores de pagos
- **Entity type:** `Payment` (open type: accepts dynamic/UDF properties)
- **Key:** `DocEntry` (Edm.Int32)
- **DB tables (main / lines):** [OPDF](../../Tablas%20SAP%20B1/OPDF.md), [PDF1](../../Tablas%20SAP%20B1/PDF1.md), [PDF2](../../Tablas%20SAP%20B1/PDF2.md)
- **ETag / optimistic concurrency:** No
- **Other entity sets with the same type:** [VendorPayments](VendorPayments.md), [IncomingPayments](IncomingPayments.md)
- **Properties:** 110 · **Navigation properties:** 14 · **Bound actions:** 4

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/PaymentDrafts?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/PaymentDrafts/$count` | Contar |
| Get by key | `GET /b1s/v2/PaymentDrafts(1)` | Obtener por clave |
| Create | `POST /b1s/v2/PaymentDrafts` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/PaymentDrafts(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/PaymentDrafts(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/PaymentDrafts(1)` (only if the B1 object allows removal) | Borrar |
| Action `Cancel` | `POST /b1s/v2/PaymentDrafts(1)/Cancel` | Cancelar |
| Action `SaveDraftToDocument` | `POST /b1s/v2/PaymentDrafts(1)/SaveDraftToDocument` | Guardar borrador como documento |
| Action `CancelbyCurrentSystemDate` | `POST /b1s/v2/PaymentDrafts(1)/CancelbyCurrentSystemDate` | Cancelar con la fecha actual del sistema |
| Action `RequestApproveCancellation` | `POST /b1s/v2/PaymentDrafts(1)/RequestApproveCancellation` | Solicitar aprobación de cancelación |

## Properties (110)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocNum` | Edm.Int32 | Yes | Document Number | Número de documento |
| 2 | `DocType` | [BoRcptTypes](../Enums/BoRcptTypes.md) | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 3 | `HandWritten` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Hand Written | Manual (numeración manual) |
| 4 | `Printed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Printed | Impreso |
| 5 | `DocDate` | Edm.DateTimeOffset | Yes | Document Date | Fecha de contabilización del documento |
| 6 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 7 | `CardName` | Edm.String | Yes | Card Name | Nombre del socio de negocios |
| 8 | `Address` | Edm.String | Yes | Address | Dirección |
| 9 | `CashAccount` | Edm.String | Yes | Cash Account | Cuenta de caja |
| 10 | `DocCurrency` | Edm.String | Yes | Document Currency | Moneda del documento |
| 11 | `CashSum` | Edm.Double | Yes | Cash Sum | Importe en efectivo |
| 12 | `CheckAccount` | Edm.String | Yes | Check Account | Cuenta del cheque |
| 13 | `TransferAccount` | Edm.String | Yes | Transfer Account | Cuenta de transferencia |
| 14 | `TransferSum` | Edm.Double | Yes | Transfer Sum | Importe de transferencia |
| 15 | `TransferDate` | Edm.DateTimeOffset | Yes | Transfer Date | Fecha de transferencia |
| 16 | `TransferReference` | Edm.String | Yes | Transfer Reference | Referencia de la transferencia |
| 17 | `LocalCurrency` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Local Currency | Moneda local |
| 18 | `DocRate` | Edm.Double | Yes | Document Rate | Tipo de cambio del documento |
| 19 | `Reference1` | Edm.String | Yes | Reference 1 | Referencia 1 |
| 20 | `Reference2` | Edm.String | Yes | Reference 2 | Referencia 2 |
| 21 | `CounterReference` | Edm.String | Yes | Counter Reference | Referencia del contador |
| 22 | `PaymentReferenceNo` | Edm.String | Yes | Payment Reference Number | N.º de referencia del pago |
| 23 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 24 | `JournalRemarks` | Edm.String | Yes | Journal Remarks | Comentarios del asiento |
| 25 | `SplitTransaction` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Split Transaction | Dividir transacción |
| 26 | `ContactPersonCode` | Edm.Int32 | Yes | Contact Person Code | Código de persona de contacto |
| 27 | `ApplyVAT` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Apply VAT | Aplicar IVA |
| 28 | `TaxDate` | Edm.DateTimeOffset | Yes | Tax Date | Fecha del documento (fecha de impuestos) |
| 29 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 30 | `BankCode` | Edm.String | Yes | Bank Code | Código del banco |
| 31 | `BankAccount` | Edm.String | Yes | Bank Account | Cuenta bancaria |
| 32 | `DiscountPercent` | Edm.Double | Yes | Discount Percent | Porcentaje de descuento |
| 33 | `ProjectCode` | Edm.String | Yes | Project Code | Código de proyecto |
| 34 | `CurrencyIsLocal` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Currency Is Local | Moneda es local |
| 35 | `DeductionPercent` | Edm.Double | Yes | Deduction Percent | Porcentaje de deducción |
| 36 | `DeductionSum` | Edm.Double | Yes | Deduction Sum | Importe de deducción |
| 37 | `CashSumFC` | Edm.Double | Yes | Cash Sum FC (foreign currency) | Importe en efectivo (ME) |
| 38 | `CashSumSys` | Edm.Double | Yes | Cash Sum (system currency) | Importe en efectivo (moneda del sistema) |
| 39 | `BoeAccount` | Edm.String | Yes | Boe Account | Cuenta de letra de cambio |
| 40 | `BillOfExchangeAmount` | Edm.Double | Yes | Bill Of Exchange Amount | Importe de letra de cambio |
| 41 | `BillofExchangeStatus` | [BoBoeStatus](../Enums/BoBoeStatus.md) | Yes | Billof Exchange Status | Estado de la letra de cambio |
| 42 | `BillOfExchangeAmountFC` | Edm.Double | Yes | Bill Of Exchange Amount FC (foreign currency) | Importe de letra de cambio (ME) |
| 43 | `BillOfExchangeAmountSC` | Edm.Double | Yes | Bill Of Exchange Amount SC (system currency) | Importe de letra de cambio (moneda del sistema) |
| 44 | `BillOfExchangeAgent` | Edm.String | Yes | Bill Of Exchange Agent | Agente de letra de cambio |
| 45 | `WTCode` | Edm.String | Yes | Withholding Tax Code | Código de retención |
| 46 | `WTAmount` | Edm.Double | Yes | Withholding Tax Amount | Importe de retención |
| 47 | `WTAmountFC` | Edm.Double | Yes | Withholding Tax Amount FC (foreign currency) | Importe de retención (ME) |
| 48 | `WTAmountSC` | Edm.Double | Yes | Withholding Tax Amount SC (system currency) | Importe de retención (moneda del sistema) |
| 49 | `WTAccount` | Edm.String | Yes | Withholding Tax Account | Cuenta de retención |
| 50 | `WTTaxableAmount` | Edm.Double | Yes | Withholding Tax Taxable Amount | Importe imponible de retención |
| 51 | `Proforma` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Proforma | Proforma |
| 52 | `PayToBankCode` | Edm.String | Yes | Pay To Bank Code | Código del banco de pago |
| 53 | `PayToBankBranch` | Edm.String | Yes | Pay To Bank Branch | Sucursal del banco de pago |
| 54 | `PayToBankAccountNo` | Edm.String | Yes | Pay To Bank Account Number | N.º de cuenta del banco de pago |
| 55 | `PayToCode` | Edm.String | Yes | Pay To Code | Código de dirección de pago (facturación) |
| 56 | `PayToBankCountry` | Edm.String | Yes | Pay To Bank Country | País del banco de pago |
| 57 | `IsPayToBank` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Pay To Bank | Es banco de pago |
| 58 | `DocEntry` 🔑 | Edm.Int32 | No | Document Entry | DocEntry (clave interna del documento) |
| 59 | `PaymentPriority` | [BoPaymentPriorities](../Enums/BoPaymentPriorities.md) | Yes | Payment Priority | Prioridad de pago |
| 60 | `TaxGroup` | Edm.String | Yes | Tax Group | Grupo de impuestos |
| 61 | `BankChargeAmount` | Edm.Double | Yes | Bank Charge Amount | Importe de comisión bancaria |
| 62 | `BankChargeAmountInFC` | Edm.Double | Yes | Bank Charge Amount In FC (foreign currency) | Importe de comisión bancaria (ME) |
| 63 | `BankChargeAmountInSC` | Edm.Double | Yes | Bank Charge Amount In SC (system currency) | Importe de comisión bancaria (moneda del sistema) |
| 64 | `UnderOverpaymentdifference` | Edm.Double | Yes | Under Overpaymentdifference | Diferencia por pago de menos/de más |
| 65 | `UnderOverpaymentdiffSC` | Edm.Double | Yes | Under Overpaymentdiff SC (system currency) | Diferencia por pago de menos/de más (moneda del sistema) |
| 66 | `WtBaseSum` | Edm.Double | Yes | Wt Base Sum | Importe base de retención |
| 67 | `WtBaseSumFC` | Edm.Double | Yes | Wt Base Sum FC (foreign currency) | Importe base de retención (ME) |
| 68 | `WtBaseSumSC` | Edm.Double | Yes | Wt Base Sum SC (system currency) | Importe base de retención (moneda del sistema) |
| 69 | `VatDate` | Edm.DateTimeOffset | Yes | Vat Date | Fecha de IVA |
| 70 | `TransactionCode` | Edm.String | Yes | Transaction Code | Código de transacción |
| 71 | `PaymentType` | [BoORCTPaymentTypeEnum](../Enums/BoORCTPaymentTypeEnum.md) | Yes | Payment Type | Tipo de pago |
| 72 | `TransferRealAmount` | Edm.Double | Yes | Transfer Real Amount | Importe real de transferencia |
| 73 | `DocObjectCode` | [BoPaymentsObjectType](../Enums/BoPaymentsObjectType.md) | Yes | Document Object Code | Código de objeto del documento |
| 74 | `DocTypte` | [BoRcptTypes](../Enums/BoRcptTypes.md) | Yes | Document Typte | Tipo de documento |
| 75 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 76 | `LocationCode` | Edm.Int32 | Yes | Location Code | Código de ubicación |
| 77 | `Cancelled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Cancelled | Cancelado |
| 78 | `CancelStatus` | [CancelStatusEnum](../Enums/CancelStatusEnum.md) | Yes | Cancel Status | Estado de cancelación |
| 79 | `ControlAccount` | Edm.String | Yes | Control Account | Cuenta asociada |
| 80 | `UnderOverpaymentdiffFC` | Edm.Double | Yes | Under Overpaymentdiff FC (foreign currency) | Diferencia por pago de menos/de más (ME) |
| 81 | `AuthorizationStatus` | [PaymentsAuthorizationStatusEnum](../Enums/PaymentsAuthorizationStatusEnum.md) | Yes | Authorization Status | Estado de autorización |
| 82 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |
| 83 | `BPLName` | Edm.String | Yes | Branch Name | Nombre de la sucursal |
| 84 | `VATRegNum` | Edm.String | Yes | VAT Reg Number | Número de registro de IVA |
| 85 | `BlanketAgreement` | Edm.Int32 | Yes | Blanket Agreement | Acuerdo global |
| 86 | `PaymentByWTCertif` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Payment By Withholding Tax Certif | Pago por certificado de retención |
| 87 | `Cig` | Edm.Int32 | Yes | Cig | Código CIG |
| 88 | `Cup` | Edm.Int32 | Yes | Cup | Código CUP |
| 89 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 90 | `SignatureInputMessage` | Edm.String | Yes | Signature Input Message | Mensaje de entrada de la firma |
| 91 | `SignatureDigest` | Edm.String | Yes | Signature Digest | Resumen de firma |
| 92 | `CertificationNumber` | Edm.String | Yes | Certification Number | Número de certificación |
| 93 | `PrivateKeyVersion` | Edm.Int32 | Yes | Private Key Version | Versión de clave privada |
| 94 | `EDocExportFormat` | Edm.Int32 | Yes | E Document Export Format | Formato de exportación del documento electrónico |
| 95 | `ElecCommStatus` | [ElecCommStatusEnum](../Enums/ElecCommStatusEnum.md) | Yes | Elec Comm Status | Estado de comunicación electrónica |
| 96 | `ElecCommMessage` | Edm.String | Yes | Elec Comm Message | Mensaje de comunicación electrónica |
| 97 | `SplitVendorCreditRow` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Split Vendor Credit Row | Dividir línea de crédito del proveedor |
| 98 | `DigitalPayments` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Digital Payments | Pagos digitales |
| 99 | `AllocationNumberIL` | Edm.String | Yes | Allocation Number IL | Número de asignación (Israel) |
| 100 | `PaymentChecks` | Collection([PaymentCheck](../Tipos-Complejos/PaymentCheck.md)) | Yes | Payment Checks | Cheques del pago |
| 101 | `PaymentInvoices` | Collection([PaymentInvoice](../Tipos-Complejos/PaymentInvoice.md)) | Yes | Payment Invoices | Facturas del pago |
| 102 | `PaymentCreditCards` | Collection([PaymentCreditCard](../Tipos-Complejos/PaymentCreditCard.md)) | Yes | Payment Credit Cards | Tarjetas de crédito del pago |
| 103 | `PaymentAccounts` | Collection([PaymentAccount](../Tipos-Complejos/PaymentAccount.md)) | Yes | Payment Accounts | Cuentas del pago |
| 104 | `PaymentDocumentReferencesCollection` | Collection([PaymentDocumentReferences](../Tipos-Complejos/PaymentDocumentReferences.md)) | Yes | Payment Document References Collection | Referencias de documentos del pago |
| 105 | `BillOfExchange` | [BillOfExchange](../Tipos-Complejos/BillOfExchange.md) | Yes | Bill Of Exchange | Letra de cambio |
| 106 | `WithholdingTaxCertificatesCollection` | Collection([WithholdingTaxCertificatesData](../Tipos-Complejos/WithholdingTaxCertificatesData.md)) | Yes | Withholding Tax Certificates Collection | Colección de certificados de retención |
| 107 | `ElectronicProtocols` | Collection([ElectronicProtocol](../Tipos-Complejos/ElectronicProtocol.md)) | Yes | Electronic Protocols | Protocolos electrónicos |
| 108 | `CashFlowAssignments` | Collection([CashFlowAssignment](../Tipos-Complejos/CashFlowAssignment.md)) | Yes | Cash Flow Assignments | Asignaciones de flujo de caja |
| 109 | `Payments_ApprovalRequests` | Collection([Payments_ApprovalRequest](../Tipos-Complejos/Payments_ApprovalRequest.md)) | Yes | Payments Approval Requests | Solicitudes de autorización del pago |
| 110 | `WithholdingTaxDataWTXCollection` | Collection([WithholdingTaxDataWTX](../Tipos-Complejos/WithholdingTaxDataWTX.md)) | Yes | Withholding Tax Data WTX Collection | Colección de datos de retención WTX |

## Navigation properties (14)

Use `GET /b1s/v2/PaymentDrafts(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CardCode → CardCode | Socio de negocios |
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | CashAccount → Code | Plan de cuentas (cuentas de mayor) |
| `Currency` | [Currency](../Entidades/Currencies.md) | [Currencies](Currencies.md) | DocCurrency → Code | Moneda |
| `Project` | [Project](../Entidades/Projects.md) | [Projects](Projects.md) | ProjectCode → Code | Proyecto |
| `WithholdingTaxCode` | [WithholdingTaxCode](../Entidades/WithholdingTaxCodes.md) | [WithholdingTaxCodes](WithholdingTaxCodes.md) | WTCode → WTCode | Códigos de retención de impuestos |
| `Country` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | PayToBankCountry → Code | País |
| `VatGroup` | [VatGroup](../Entidades/VatGroups.md) | [VatGroups](VatGroups.md) | TaxGroup → Code | Grupo de IVA (indicador de impuesto) |
| `TransactionCode2` | [TransactionCode](../Entidades/TransactionCodes.md) | [TransactionCodes](TransactionCodes.md) | TransactionCode → Code | Códigos de transacción |
| `WarehouseLocation` | [WarehouseLocation](../Entidades/WarehouseLocations.md) | [WarehouseLocations](WarehouseLocations.md) | LocationCode → Code | Ubicaciones de almacenes |
| `BusinessPlace` | [BusinessPlace](../Entidades/BusinessPlaces.md) | [BusinessPlaces](BusinessPlaces.md) | BPLID → BPLID | Lugar de negocios |
| `BlanketAgreement2` | [BlanketAgreement](../Entidades/BlanketAgreements.md) | [BlanketAgreements](BlanketAgreements.md) | BlanketAgreement → AgreementNo | Acuerdos globales |
| `CIGCode` | [CIGCode](../Entidades/CIGCodes.md) | [CIGCodes](CIGCodes.md) | Cig → AbsEntry | Códigos CIG |
| `CUPCode` | [CUPCode](../Entidades/CUPCodes.md) | [CUPCodes](CUPCodes.md) | Cup → AbsEntry | Códigos CUP |
| `Attachments2` | [Attachments2](../Entidades/Attachments2.md) | [Attachments2](Attachments2.md) | AttachmentEntry → AbsoluteEntry | Anexos |

## Bound actions (4)

### Cancel

- **Descripción (ES):** Cancelar
- **Request:** `POST /b1s/v2/PaymentDrafts(1)/Cancel`

### SaveDraftToDocument

- **Descripción (ES):** Guardar borrador como documento
- **Request:** `POST /b1s/v2/PaymentDrafts(1)/SaveDraftToDocument`

### CancelbyCurrentSystemDate

- **Descripción (ES):** Cancelar con la fecha actual del sistema
- **Request:** `POST /b1s/v2/PaymentDrafts(1)/CancelbyCurrentSystemDate`

### RequestApproveCancellation

- **Descripción (ES):** Solicitar aprobación de cancelación
- **Request:** `POST /b1s/v2/PaymentDrafts(1)/RequestApproveCancellation`

