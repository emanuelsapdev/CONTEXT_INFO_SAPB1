# JournalEntries — Asientos contables

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `JournalEntries`
- **Descripción (ES):** Asientos contables
- **Entity type:** `JournalEntry` (open type: accepts dynamic/UDF properties)
- **Key:** `JdtNum` (Edm.Int32)
- **DB tables (main / lines):** [OJDT](../../Tablas%20SAP%20B1/OJDT.md), [JDT1](../../Tablas%20SAP%20B1/JDT1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 62 · **Navigation properties:** 38 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/JournalEntries?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/JournalEntries/$count` | Contar |
| Get by key | `GET /b1s/v2/JournalEntries(1)` | Obtener por clave |
| Create | `POST /b1s/v2/JournalEntries` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/JournalEntries(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/JournalEntries(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/JournalEntries(1)` (only if the B1 object allows removal) | Borrar |
| Action `Cancel` | `POST /b1s/v2/JournalEntries(1)/Cancel` | Cancelar |

## Properties (62)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ReferenceDate` | Edm.DateTimeOffset | Yes | Reference Date | Fecha de referencia |
| 2 | `Memo` | Edm.String | Yes | Memo | Comentario |
| 3 | `Reference` | Edm.String | Yes | Reference | Referencia |
| 4 | `Reference2` | Edm.String | Yes | Reference 2 | Referencia 2 |
| 5 | `TransactionCode` | Edm.String | Yes | Transaction Code | Código de transacción |
| 6 | `ProjectCode` | Edm.String | Yes | Project Code | Código de proyecto |
| 7 | `TaxDate` | Edm.DateTimeOffset | Yes | Tax Date | Fecha del documento (fecha de impuestos) |
| 8 | `JdtNum` 🔑 | Edm.Int32 | No | Jdt Number | Número de asiento |
| 9 | `Indicator` | Edm.String | Yes | Indicator | Indicador |
| 10 | `UseAutoStorno` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Auto Storno | Usar anulación automática |
| 11 | `StornoDate` | Edm.DateTimeOffset | Yes | Storno Date | Fecha de anulación (storno) |
| 12 | `VatDate` | Edm.DateTimeOffset | Yes | Vat Date | Fecha de IVA |
| 13 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 14 | `StampTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Stamp Tax | Impuesto de timbre |
| 15 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 16 | `AutoVAT` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Auto VAT | IVA automático |
| 17 | `Number` | Edm.Int32 | Yes | Number | Número |
| 18 | `FolioNumber` | Edm.Int32 | Yes | Folio Number | Número de folio |
| 19 | `FolioPrefixString` | Edm.String | Yes | Folio Prefix String | Prefijo de folio (letra) |
| 20 | `ReportEU` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Report EU | Informe UE |
| 21 | `Report347` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Report 347 | Modelo 347 |
| 22 | `Printed` | [PrintStatusEnum](../Enums/PrintStatusEnum.md) | Yes | Printed | Impreso |
| 23 | `LocationCode` | Edm.Int32 | Yes | Location Code | Código de ubicación |
| 24 | `OriginalJournal` | [TransTypesEnum](../Enums/TransTypesEnum.md) | Yes | Original Journal | Asiento original |
| 25 | `Original` | Edm.Int32 | Yes | Original | Original |
| 26 | `BaseReference` | Edm.String | Yes | Base Reference | Referencia base |
| 27 | `BlockDunningLetter` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Dunning Letter | Bloquear carta de reclamación |
| 28 | `AutomaticWT` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Automatic Withholding Tax | Retención automática |
| 29 | `WTSum` | Edm.Double | Yes | Withholding Tax Sum | Importe de retención |
| 30 | `WTSumSC` | Edm.Double | Yes | Withholding Tax Sum SC (system currency) | Importe de retención (moneda del sistema) |
| 31 | `WTSumFC` | Edm.Double | Yes | Withholding Tax Sum FC (foreign currency) | Importe de retención (ME) |
| 32 | `SignatureInputMessage` | Edm.String | Yes | Signature Input Message | Mensaje de entrada de la firma |
| 33 | `SignatureDigest` | Edm.String | Yes | Signature Digest | Resumen de firma |
| 34 | `CertificationNumber` | Edm.String | Yes | Certification Number | Número de certificación |
| 35 | `PrivateKeyVersion` | Edm.Int32 | Yes | Private Key Version | Versión de clave privada |
| 36 | `Corisptivi` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Corisptivi | Corrispettivi (Italia) |
| 37 | `Reference3` | Edm.String | Yes | Reference 3 | Referencia 3 |
| 38 | `DocumentType` | Edm.String | Yes | Document Type | Tipo de documento |
| 39 | `DeferredTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Deferred Tax | Impuesto diferido |
| 40 | `BlanketAgreementNumber` | Edm.Int32 | Yes | Blanket Agreement Number | Número de acuerdo global |
| 41 | `OperationCode` | [OperationCodeTypeEnum](../Enums/OperationCodeTypeEnum.md) | Yes | Operation Code | Código de operación |
| 42 | `ResidenceNumberType` | [ResidenceNumberTypeEnum](../Enums/ResidenceNumberTypeEnum.md) | Yes | Residence Number Type | Tipo de número de residencia |
| 43 | `ECDPostingType` | [ECDPostingTypeEnum](../Enums/ECDPostingTypeEnum.md) | Yes | ECD Posting Type | Tipo de contabilización ECD |
| 44 | `ExposedTransNumber` | Edm.Int32 | Yes | Exposed Trans Number | Número de transacción expuesto |
| 45 | `PointOfIssueCode` | Edm.String | Yes | Point Of Issue Code | Código de punto de emisión |
| 46 | `Letter` | [FolioLetterEnum](../Enums/FolioLetterEnum.md) | Yes | Letter | Carta |
| 47 | `FolioNumberFrom` | Edm.Int32 | Yes | Folio Number From | Número de folio desde |
| 48 | `FolioNumberTo` | Edm.Int32 | Yes | Folio Number To | Número de folio hasta |
| 49 | `IsCostCenterTransfer` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Cost Center Transfer | Es transferencia de centro de costo |
| 50 | `ReportingSectionControlStatementVAT` | Edm.String | Yes | Reporting Section Control Statement VAT | Sección del informe de control de IVA |
| 51 | `ExcludeFromTaxReportControlStatementVAT` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Exclude From Tax Report Control Statement VAT | Excluir del informe de control de IVA |
| 52 | `SAPPassport` | Edm.String | Yes | SAP Passport | SAP Passport |
| 53 | `Cig` | Edm.Int32 | Yes | Cig | Código CIG |
| 54 | `Cup` | Edm.Int32 | Yes | Cup | Código CUP |
| 55 | `AdjustTransaction` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Adjust Transaction | Transacción de ajuste |
| 56 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 57 | `SAFTTransactionType` | [SAFTTransactionTypeEnum](../Enums/SAFTTransactionTypeEnum.md) | Yes | SAFT Transaction Type | Tipo de transacción SAF-T |
| 58 | `AllocationNumberIL` | Edm.String | Yes | Allocation Number IL | Número de asignación (Israel) |
| 59 | `SAFTTransactionTypeEx` | Edm.String | Yes | SAFT Transaction Type Ex | Tipo de transacción SAF-T (ampliado) |
| 60 | `JournalEntryLines` | Collection([JournalEntryLine](../Tipos-Complejos/JournalEntryLine.md)) | Yes | Journal Entry Lines | Líneas del asiento contable |
| 61 | `WithholdingTaxDataCollection` | Collection([WithholdingTaxData](../Tipos-Complejos/WithholdingTaxData.md)) | Yes | Withholding Tax Data Collection | Colección de datos de retención |
| 62 | `ElectronicProtocols` | Collection([ElectronicProtocol](../Tipos-Complejos/ElectronicProtocol.md)) | Yes | Electronic Protocols | Protocolos electrónicos |

## Navigation properties (38)

Use `GET /b1s/v2/JournalEntries(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `LandedCosts` | Collection([LandedCost](../Entidades/LandedCosts.md)) | [LandedCosts](LandedCosts.md) |  | Costos de importación (landed costs) |
| `StockTransfers` | Collection([StockTransfer](../Entidades/StockTransfers.md)) | [StockTransfers](StockTransfers.md) |  | Transferencias de stock |
| `ChecksforPayment` | Collection([ChecksforPayment](../Entidades/ChecksforPayment.md)) | [ChecksforPayment](ChecksforPayment.md) |  | Cheques para pago |
| `CorrectionInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoiceReversal](CorrectionInvoiceReversal.md) |  | Anulación de factura de corrección de clientes |
| `CorrectionInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoice](CorrectionInvoice.md) |  | Factura de corrección de clientes |
| `PurchaseDeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDeliveryNotes](PurchaseDeliveryNotes.md) |  | Pedidos de entrada de mercancías |
| `CorrectionPurchaseInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoice](CorrectionPurchaseInvoice.md) |  | Factura de corrección de proveedores |
| `TransactionCode2` | [TransactionCode](../Entidades/TransactionCodes.md) | [TransactionCodes](TransactionCodes.md) | TransactionCode → Code | Códigos de transacción |
| `Project` | [Project](../Entidades/Projects.md) | [Projects](Projects.md) | ProjectCode → Code | Proyecto |
| `FactoringIndicator` | [FactoringIndicator](../Entidades/FactoringIndicators.md) | [FactoringIndicators](FactoringIndicators.md) | Indicator → IndicatorCode | Indicadores de factoring |
| `WarehouseLocation` | [WarehouseLocation](../Entidades/WarehouseLocations.md) | [WarehouseLocations](WarehouseLocations.md) | LocationCode → Code | Ubicaciones de almacenes |
| `JournalEntryDocumentType` | [JournalEntryDocumentType](../Entidades/JournalEntryDocumentTypes.md) | [JournalEntryDocumentTypes](JournalEntryDocumentTypes.md) | DocumentType → JournalEntryType | Tipos de documento de asiento |
| `BlanketAgreement` | [BlanketAgreement](../Entidades/BlanketAgreements.md) | [BlanketAgreements](BlanketAgreements.md) | BlanketAgreementNumber → AgreementNo | Acuerdo global |
| `CIGCode` | [CIGCode](../Entidades/CIGCodes.md) | [CIGCodes](CIGCodes.md) | Cig → AbsEntry | Códigos CIG |
| `CUPCode` | [CUPCode](../Entidades/CUPCodes.md) | [CUPCodes](CUPCodes.md) | Cup → AbsEntry | Códigos CUP |
| `Attachments2` | [Attachments2](../Entidades/Attachments2.md) | [Attachments2](Attachments2.md) | AttachmentEntry → AbsoluteEntry | Anexos |
| `InventoryGenEntries` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenEntries](InventoryGenEntries.md) |  | Entradas de mercancías |
| `AssetRevaluations` | Collection([AssetRevaluation](../Entidades/AssetRevaluations.md)) | [AssetRevaluations](AssetRevaluations.md) |  | Revalorizaciones de activos |
| `InventoryGenExits` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenExits](InventoryGenExits.md) |  | Salidas de mercancías |
| `MaterialRevaluation` | Collection([MaterialRevaluation](../Entidades/MaterialRevaluation.md)) | [MaterialRevaluation](MaterialRevaluation.md) |  | Revalorización de inventario |
| `Drafts` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Drafts](Drafts.md) |  | Borradores de documentos |
| `BillOfExchangeTransactions` | Collection([BillOfExchangeTransaction](../Entidades/BillOfExchangeTransactions.md)) | [BillOfExchangeTransactions](BillOfExchangeTransactions.md) |  | Transacciones de letras de cambio |
| `ReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [ReturnRequest](ReturnRequest.md) |  | Solicitudes de devolución de clientes |
| `DeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DeliveryNotes](DeliveryNotes.md) |  | Entregas |
| `PurchaseInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseInvoices](PurchaseInvoices.md) |  | Facturas de proveedores |
| `StockTransferDrafts` | Collection([StockTransfer](../Entidades/StockTransfers.md)) | [StockTransferDrafts](StockTransferDrafts.md) |  | Borradores de transferencias de stock |
| `SelfInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfInvoices](SelfInvoices.md) |  | Autofacturas |
| `Invoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Invoices](Invoices.md) |  | Facturas de clientes |
| `CreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CreditNotes](CreditNotes.md) |  | Notas de crédito de clientes |
| `PurchaseCreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseCreditNotes](PurchaseCreditNotes.md) |  | Notas de crédito de proveedores |
| `ProductionOrders` | Collection([ProductionOrder](../Entidades/ProductionOrders.md)) | [ProductionOrders](ProductionOrders.md) |  | Órdenes de fabricación |
| `DownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DownPayments](DownPayments.md) |  | Facturas de anticipo de clientes |
| `PurchaseDownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDownPayments](PurchaseDownPayments.md) |  | Facturas de anticipo de proveedores |
| `PurchaseReturns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseReturns](PurchaseReturns.md) |  | Devoluciones de mercancías a proveedores |
| `SelfCreditMemos` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfCreditMemos](SelfCreditMemos.md) |  | Autonotas de crédito |
| `Returns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Returns](Returns.md) |  | Devoluciones de clientes |
| `GoodsReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [GoodsReturnRequest](GoodsReturnRequest.md) |  | Solicitudes de devolución de mercancías |
| `CorrectionPurchaseInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoiceReversal](CorrectionPurchaseInvoiceReversal.md) |  | Anulación de factura de corrección de proveedores |

## Bound actions (1)

### Cancel

- **Descripción (ES):** Cancelar
- **Request:** `POST /b1s/v2/JournalEntries(1)/Cancel`


## Service operations that use this type

- [`JournalEntriesService_Close`](../Servicios/JournalEntriesService.md#journalentriesservice_close)
- [`JournalVouchersService_Add`](../Servicios/JournalVouchersService.md#journalvouchersservice_add)
