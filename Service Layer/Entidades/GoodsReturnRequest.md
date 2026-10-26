# GoodsReturnRequest — Solicitudes de devolución de mercancías

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `GoodsReturnRequest`
- **Descripción (ES):** Solicitudes de devolución de mercancías
- **Entity type:** `Document` (open type: accepts dynamic/UDF properties)
- **Key:** `DocEntry` (Edm.Int32)
- **DB tables (main / lines):** [OPRR](../../Tablas%20SAP%20B1/OPRR.md), [PRR1](../../Tablas%20SAP%20B1/PRR1.md)
- **ETag / optimistic concurrency:** Yes (`DataVersion`) — send `If-Match` on PATCH/DELETE/actions
- **Other entity sets with the same type:** [PurchaseQuotations](PurchaseQuotations.md), [CorrectionInvoiceReversal](CorrectionInvoiceReversal.md), [CorrectionInvoice](CorrectionInvoice.md), [PurchaseDeliveryNotes](PurchaseDeliveryNotes.md), [CorrectionPurchaseInvoice](CorrectionPurchaseInvoice.md), [InventoryGenEntries](InventoryGenEntries.md), [Orders](Orders.md), [InventoryGenExits](InventoryGenExits.md), [Drafts](Drafts.md), [ReturnRequest](ReturnRequest.md), [DeliveryNotes](DeliveryNotes.md), [PurchaseInvoices](PurchaseInvoices.md), [SelfInvoices](SelfInvoices.md), [Invoices](Invoices.md), [CreditNotes](CreditNotes.md), [PurchaseCreditNotes](PurchaseCreditNotes.md), [DownPayments](DownPayments.md), [PurchaseDownPayments](PurchaseDownPayments.md), [PurchaseReturns](PurchaseReturns.md), [PurchaseOrders](PurchaseOrders.md), [SelfCreditMemos](SelfCreditMemos.md), [Quotations](Quotations.md), [Returns](Returns.md), [CorrectionPurchaseInvoiceReversal](CorrectionPurchaseInvoiceReversal.md), [PurchaseRequests](PurchaseRequests.md)
- **Properties:** 302 · **Navigation properties:** 26 · **Bound actions:** 4

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/GoodsReturnRequest?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/GoodsReturnRequest/$count` | Contar |
| Get by key | `GET /b1s/v2/GoodsReturnRequest(1)` | Obtener por clave |
| Create | `POST /b1s/v2/GoodsReturnRequest` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/GoodsReturnRequest(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/GoodsReturnRequest(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/GoodsReturnRequest(1)` (only if the B1 object allows removal) | Borrar |
| Action `Close` | `POST /b1s/v2/GoodsReturnRequest(1)/Close` | Cerrar |
| Action `Cancel` | `POST /b1s/v2/GoodsReturnRequest(1)/Cancel` | Cancelar |
| Action `Reopen` | `POST /b1s/v2/GoodsReturnRequest(1)/Reopen` | Reabrir |
| Action `CreateCancellationDocument` | `POST /b1s/v2/GoodsReturnRequest(1)/CreateCancellationDocument` | Crear documento de cancelación |

## Properties (302)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` 🔑 | Edm.Int32 | No | Document Entry | DocEntry (clave interna del documento) |
| 2 | `DocNum` | Edm.Int32 | Yes | Document Number | Número de documento |
| 3 | `DocType` | [BoDocumentTypes](../Enums/BoDocumentTypes.md) | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 4 | `HandWritten` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Hand Written | Manual (numeración manual) |
| 5 | `Printed` | [PrintStatusEnum](../Enums/PrintStatusEnum.md) | Yes | Printed | Impreso |
| 6 | `DocDate` | Edm.DateTimeOffset | Yes | Document Date | Fecha de contabilización del documento |
| 7 | `DocDueDate` | Edm.DateTimeOffset | Yes | Document Due Date | Fecha de vencimiento del documento |
| 8 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 9 | `CardName` | Edm.String | Yes | Card Name | Nombre del socio de negocios |
| 10 | `Address` | Edm.String | Yes | Address | Dirección |
| 11 | `NumAtCard` | Edm.String | Yes | Number At Card | Número de referencia del socio de negocios |
| 12 | `DocTotal` | Edm.Double | Yes | Document Total | Total del documento |
| 13 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 14 | `DocCurrency` | Edm.String | Yes | Document Currency | Moneda del documento |
| 15 | `DocRate` | Edm.Double | Yes | Document Rate | Tipo de cambio del documento |
| 16 | `Reference1` | Edm.String | Yes | Reference 1 | Referencia 1 |
| 17 | `Reference2` | Edm.String | Yes | Reference 2 | Referencia 2 |
| 18 | `Comments` | Edm.String | Yes | Comments | Comentarios |
| 19 | `JournalMemo` | Edm.String | Yes | Journal Memo | Comentario del asiento |
| 20 | `PaymentGroupCode` | Edm.Int32 | Yes | Payment Group Code | Código de grupo de pago (condiciones de pago) |
| 21 | `DocTime` | Edm.TimeOfDay | Yes | Document Time | Hora del documento |
| 22 | `SalesPersonCode` | Edm.Int32 | Yes | Sales Person Code | Código del empleado de ventas |
| 23 | `TransportationCode` | Edm.Int32 | Yes | Transportation Code | Código de transporte |
| 24 | `Confirmed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Confirmed | Confirmado |
| 25 | `ImportFileNum` | Edm.Int32 | Yes | Import File Number | Número de archivo de importación |
| 26 | `SummeryType` | [BoDocSummaryTypes](../Enums/BoDocSummaryTypes.md) | Yes | Summery Type | Tipo de resumen |
| 27 | `ContactPersonCode` | Edm.Int32 | Yes | Contact Person Code | Código de persona de contacto |
| 28 | `ShowSCN` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Show SCN | Mostrar N.º de catálogo del socio de negocios |
| 29 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 30 | `TaxDate` | Edm.DateTimeOffset | Yes | Tax Date | Fecha del documento (fecha de impuestos) |
| 31 | `PartialSupply` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Partial Supply | Suministro parcial |
| 32 | `DocObjectCode` | [BoObjectTypes](../Enums/BoObjectTypes.md) | Yes | Document Object Code | Código de objeto del documento |
| 33 | `ShipToCode` | Edm.String | Yes | Ship To Code | Código de dirección de envío |
| 34 | `Indicator` | Edm.String | Yes | Indicator | Indicador |
| 35 | `FederalTaxID` | Edm.String | Yes | Federal Tax ID | CUIT / ID fiscal federal |
| 36 | `DiscountPercent` | Edm.Double | Yes | Discount Percent | Porcentaje de descuento |
| 37 | `PaymentReference` | Edm.String | Yes | Payment Reference | Referencia del pago |
| 38 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 39 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 40 | `FinancialPeriod` | Edm.Int32 | Yes | Financial Period | Período contable |
| 41 | `UserSign` | Edm.Int32 | Yes | User Sign | Usuario que creó (firma) |
| 42 | `TransNum` | Edm.Int32 | Yes | Trans Number | Número de transacción |
| 43 | `VatSum` | Edm.Double | Yes | Vat Sum | Importe de IVA |
| 44 | `VatSumSys` | Edm.Double | Yes | Vat Sum (system currency) | Importe de IVA (moneda del sistema) |
| 45 | `VatSumFc` | Edm.Double | Yes | Vat Sum Fc | Importe de IVA (ME) |
| 46 | `NetProcedure` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Net Procedure | Procedimiento neto |
| 47 | `DocTotalFc` | Edm.Double | Yes | Document Total Fc | Total del documento (ME) |
| 48 | `DocTotalSys` | Edm.Double | Yes | Document Total (system currency) | Total del documento (moneda del sistema) |
| 49 | `Form1099` | Edm.Int32 | Yes | Form 1099 | Formulario 1099 |
| 50 | `Box1099` | Edm.String | Yes | Box 1099 | Casilla 1099 |
| 51 | `RevisionPo` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Revision Po | Revisión del pedido de compra |
| 52 | `RequriedDate` | Edm.DateTimeOffset | Yes | Requried Date | Fecha requerida |
| 53 | `CancelDate` | Edm.DateTimeOffset | Yes | Cancel Date | Fecha de cancelación |
| 54 | `BlockDunning` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Dunning | Bloquear reclamaciones |
| 55 | `Submitted` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Submitted | Enviado |
| 56 | `Segment` | Edm.Int32 | Yes | Segment | Segmento |
| 57 | `PickStatus` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Pick Status | Estado de picking |
| 58 | `Pick` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Pick | Picking |
| 59 | `PaymentMethod` | Edm.String | Yes | Payment Method | Vía de pago |
| 60 | `PaymentBlock` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Payment Block | Bloqueo de pago |
| 61 | `PaymentBlockEntry` | Edm.Int32 | Yes | Payment Block Entry | Entrada del bloqueo de pago |
| 62 | `CentralBankIndicator` | Edm.String | Yes | Central Bank Indicator | Indicador del banco central |
| 63 | `MaximumCashDiscount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Maximum Cash Discount | Descuento por pronto pago máximo |
| 64 | `Reserve` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reserve | Reserva |
| 65 | `Project` | Edm.String | Yes | Project | Proyecto |
| 66 | `ExemptionValidityDateFrom` | Edm.DateTimeOffset | Yes | Exemption Validity Date From | Validez de exención desde |
| 67 | `ExemptionValidityDateTo` | Edm.DateTimeOffset | Yes | Exemption Validity Date To | Validez de exención hasta |
| 68 | `WareHouseUpdateType` | [BoDocWhsUpdateTypes](../Enums/BoDocWhsUpdateTypes.md) | Yes | Ware House Update Type | Tipo de actualización de almacén |
| 69 | `Rounding` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Rounding | Redondeo |
| 70 | `ExternalCorrectedDocNum` | Edm.String | Yes | External Corrected Document Number | N.º de documento corregido externo |
| 71 | `InternalCorrectedDocNum` | Edm.Int32 | Yes | Internal Corrected Document Number | N.º de documento corregido interno |
| 72 | `NextCorrectingDocument` | Edm.Int32 | Yes | Next Correcting Document | Siguiente documento de corrección |
| 73 | `DeferredTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Deferred Tax | Impuesto diferido |
| 74 | `TaxExemptionLetterNum` | Edm.String | Yes | Tax Exemption Letter Number | N.º de carta de exención de impuestos |
| 75 | `WTApplied` | Edm.Double | Yes | Withholding Tax Applied | Retención aplicada |
| 76 | `WTAppliedFC` | Edm.Double | Yes | Withholding Tax Applied FC (foreign currency) | Retención aplicada (ME) |
| 77 | `BillOfExchangeReserved` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Bill Of Exchange Reserved | Letra de cambio reservada |
| 78 | `AgentCode` | Edm.String | Yes | Agent Code | Código de agente |
| 79 | `WTAppliedSC` | Edm.Double | Yes | Withholding Tax Applied SC (system currency) | Retención aplicada (moneda del sistema) |
| 80 | `TotalEqualizationTax` | Edm.Double | Yes | Total Equalization Tax | Recargo de equivalencia total |
| 81 | `TotalEqualizationTaxFC` | Edm.Double | Yes | Total Equalization Tax FC (foreign currency) | Recargo de equivalencia total (ME) |
| 82 | `TotalEqualizationTaxSC` | Edm.Double | Yes | Total Equalization Tax SC (system currency) | Recargo de equivalencia total (moneda del sistema) |
| 83 | `NumberOfInstallments` | Edm.Int32 | Yes | Number Of Installments | Cantidad de cuotas |
| 84 | `ApplyTaxOnFirstInstallment` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Apply Tax On First Installment | Aplicar impuesto en la primera cuota |
| 85 | `TaxOnInstallments` | [BoTaxOnInstallmentsTypeEnum](../Enums/BoTaxOnInstallmentsTypeEnum.md) | Yes | Tax On Installments | Impuesto sobre cuotas |
| 86 | `WTNonSubjectAmount` | Edm.Double | Yes | Withholding Tax Non Subject Amount | Importe no sujeto a retención |
| 87 | `WTNonSubjectAmountSC` | Edm.Double | Yes | Withholding Tax Non Subject Amount SC (system currency) | Importe no sujeto a retención (moneda del sistema) |
| 88 | `WTNonSubjectAmountFC` | Edm.Double | Yes | Withholding Tax Non Subject Amount FC (foreign currency) | Importe no sujeto a retención (ME) |
| 89 | `WTExemptedAmount` | Edm.Double | Yes | Withholding Tax Exempted Amount | Importe exento de retención |
| 90 | `WTExemptedAmountSC` | Edm.Double | Yes | Withholding Tax Exempted Amount SC (system currency) | Importe exento de retención (moneda del sistema) |
| 91 | `WTExemptedAmountFC` | Edm.Double | Yes | Withholding Tax Exempted Amount FC (foreign currency) | Importe exento de retención (ME) |
| 92 | `BaseAmount` | Edm.Double | Yes | Base Amount | Importe base |
| 93 | `BaseAmountSC` | Edm.Double | Yes | Base Amount SC (system currency) | Importe base (moneda del sistema) |
| 94 | `BaseAmountFC` | Edm.Double | Yes | Base Amount FC (foreign currency) | Importe base (ME) |
| 95 | `WTAmount` | Edm.Double | Yes | Withholding Tax Amount | Importe de retención |
| 96 | `WTAmountSC` | Edm.Double | Yes | Withholding Tax Amount SC (system currency) | Importe de retención (moneda del sistema) |
| 97 | `WTAmountFC` | Edm.Double | Yes | Withholding Tax Amount FC (foreign currency) | Importe de retención (ME) |
| 98 | `VatDate` | Edm.DateTimeOffset | Yes | Vat Date | Fecha de IVA |
| 99 | `DocumentsOwner` | Edm.Int32 | Yes | Documents Owner | Titular del documento |
| 100 | `FolioPrefixString` | Edm.String | Yes | Folio Prefix String | Prefijo de folio (letra) |
| 101 | `FolioNumber` | Edm.Int32 | Yes | Folio Number | Número de folio |
| 102 | `DocumentSubType` | [BoDocumentSubType](../Enums/BoDocumentSubType.md) | Yes | Document Sub Type | Subtipo de documento |
| 103 | `BPChannelCode` | Edm.String | Yes | Business Partner Channel Code | Código de socio de canal |
| 104 | `BPChannelContact` | Edm.Int32 | Yes | Business Partner Channel Contact | Contacto del socio de canal |
| 105 | `Address2` | Edm.String | Yes | Address 2 | Dirección 2 |
| 106 | `DocumentStatus` | [BoStatus](../Enums/BoStatus.md) | Yes | Document Status | Estado del documento |
| 107 | `PeriodIndicator` | Edm.String | Yes | Period Indicator | Indicador de período |
| 108 | `PayToCode` | Edm.String | Yes | Pay To Code | Código de dirección de pago (facturación) |
| 109 | `ManualNumber` | Edm.String | Yes | Manual Number | Número manual |
| 110 | `UseShpdGoodsAct` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Shpd Goods Act | Usar cuenta de mercancías enviadas |
| 111 | `IsPayToBank` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Pay To Bank | Es banco de pago |
| 112 | `PayToBankCountry` | Edm.String | Yes | Pay To Bank Country | País del banco de pago |
| 113 | `PayToBankCode` | Edm.String | Yes | Pay To Bank Code | Código del banco de pago |
| 114 | `PayToBankAccountNo` | Edm.String | Yes | Pay To Bank Account Number | N.º de cuenta del banco de pago |
| 115 | `PayToBankBranch` | Edm.String | Yes | Pay To Bank Branch | Sucursal del banco de pago |
| 116 | `BPL_IDAssignedToInvoice` | Edm.Int32 | Yes | Branch ID Assigned To Invoice | ID de sucursal asignada a la factura |
| 117 | `DownPayment` | Edm.Double | Yes | Down Payment | Anticipo |
| 118 | `ReserveInvoice` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reserve Invoice | Factura de reserva |
| 119 | `LanguageCode` | Edm.Int32 | Yes | Language Code | Código de idioma |
| 120 | `TrackingNumber` | Edm.String | Yes | Tracking Number | Número de seguimiento |
| 121 | `PickRemark` | Edm.String | Yes | Pick Remark | Comentario de picking |
| 122 | `ClosingDate` | Edm.DateTimeOffset | Yes | Closing Date | Fecha de cierre |
| 123 | `SequenceCode` | Edm.Int32 | Yes | Sequence Code | Código de secuencia |
| 124 | `SequenceSerial` | Edm.Int32 | Yes | Sequence Serial | Serie de la secuencia |
| 125 | `SeriesString` | Edm.String | Yes | Series String | Cadena de la serie (prefijo) |
| 126 | `SubSeriesString` | Edm.String | Yes | Sub Series String | Cadena de la subserie |
| 127 | `SequenceModel` | Edm.String | Yes | Sequence Model | Modelo de secuencia |
| 128 | `UseCorrectionVATGroup` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Correction VAT Group | Usar grupo de IVA de corrección |
| 129 | `TotalDiscount` | Edm.Double | Yes | Total Discount | Descuento total |
| 130 | `DownPaymentAmount` | Edm.Double | Yes | Down Payment Amount | Importe del anticipo |
| 131 | `DownPaymentPercentage` | Edm.Double | Yes | Down Payment Percentage | Porcentaje de anticipo |
| 132 | `DownPaymentType` | [DownPaymentTypeEnum](../Enums/DownPaymentTypeEnum.md) | Yes | Down Payment Type | Tipo de anticipo |
| 133 | `DownPaymentAmountSC` | Edm.Double | Yes | Down Payment Amount SC (system currency) | Importe del anticipo (moneda del sistema) |
| 134 | `DownPaymentAmountFC` | Edm.Double | Yes | Down Payment Amount FC (foreign currency) | Importe del anticipo (ME) |
| 135 | `VatPercent` | Edm.Double | Yes | Vat Percent | Porcentaje de IVA |
| 136 | `ServiceGrossProfitPercent` | Edm.Double | Yes | Service Gross Profit Percent | Porcentaje de margen bruto de servicios |
| 137 | `OpeningRemarks` | Edm.String | Yes | Opening Remarks | Comentarios de apertura |
| 138 | `ClosingRemarks` | Edm.String | Yes | Closing Remarks | Comentarios de cierre |
| 139 | `RoundingDiffAmount` | Edm.Double | Yes | Rounding Diff Amount | Importe de diferencia por redondeo |
| 140 | `RoundingDiffAmountFC` | Edm.Double | Yes | Rounding Diff Amount FC (foreign currency) | Importe de diferencia por redondeo (ME) |
| 141 | `RoundingDiffAmountSC` | Edm.Double | Yes | Rounding Diff Amount SC (system currency) | Importe de diferencia por redondeo (moneda del sistema) |
| 142 | `Cancelled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Cancelled | Cancelado |
| 143 | `SignatureInputMessage` | Edm.String | Yes | Signature Input Message | Mensaje de entrada de la firma |
| 144 | `SignatureDigest` | Edm.String | Yes | Signature Digest | Resumen de firma |
| 145 | `CertificationNumber` | Edm.String | Yes | Certification Number | Número de certificación |
| 146 | `PrivateKeyVersion` | Edm.Int32 | Yes | Private Key Version | Versión de clave privada |
| 147 | `ControlAccount` | Edm.String | Yes | Control Account | Cuenta asociada |
| 148 | `InsuranceOperation347` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Insurance Operation 347 | Operación de seguros (modelo 347) |
| 149 | `ArchiveNonremovableSalesQuotation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Archive Nonremovable Sales Quotation | Archivar ofertas de ventas no eliminables |
| 150 | `GTSChecker` | Edm.Int32 | Yes | GTS Checker | Verificador GTS |
| 151 | `GTSPayee` | Edm.Int32 | Yes | GTS Payee | Beneficiario GTS |
| 152 | `ExtraMonth` | Edm.Int32 | Yes | Extra Month | Mes adicional |
| 153 | `ExtraDays` | Edm.Int32 | Yes | Extra Days | Días adicionales |
| 154 | `CashDiscountDateOffset` | Edm.Int32 | Yes | Cash Discount Date Offset | Desplazamiento de fecha de descuento por pronto pago |
| 155 | `StartFrom` | [BoPayTermDueTypes](../Enums/BoPayTermDueTypes.md) | Yes | Start From | Comenzar desde |
| 156 | `NTSApproved` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | NTS Approved | Aprobado por NTS |
| 157 | `ETaxWebSite` | Edm.Int32 | Yes | E Tax Web Site | Sitio web de impuestos electrónicos |
| 158 | `ETaxNumber` | Edm.String | Yes | E Tax Number | Número de impuesto electrónico |
| 159 | `NTSApprovedNumber` | Edm.String | Yes | NTS Approved Number | Número aprobado por NTS |
| 160 | `EDocGenerationType` | [EDocGenerationTypeEnum](../Enums/EDocGenerationTypeEnum.md) | Yes | E Document Generation Type | Tipo de generación del documento electrónico |
| 161 | `EDocSeries` | Edm.Int32 | Yes | E Document Series | Serie del documento electrónico |
| 162 | `EDocNum` | Edm.String | Yes | E Document Number | Número del documento electrónico |
| 163 | `EDocExportFormat` | Edm.Int32 | Yes | E Document Export Format | Formato de exportación del documento electrónico |
| 164 | `EDocStatus` | [EDocStatusEnum](../Enums/EDocStatusEnum.md) | Yes | E Document Status | Estado del documento electrónico |
| 165 | `EDocErrorCode` | Edm.String | Yes | E Document Error Code | Código de error del documento electrónico |
| 166 | `EDocErrorMessage` | Edm.String | Yes | E Document Error Message | Mensaje de error del documento electrónico |
| 167 | `DownPaymentStatus` | [BoSoStatus](../Enums/BoSoStatus.md) | Yes | Down Payment Status | Estado del anticipo |
| 168 | `GroupSeries` | Edm.Int32 | Yes | Group Series | Serie del grupo |
| 169 | `GroupNumber` | Edm.Int32 | Yes | Group Number | Número de grupo |
| 170 | `GroupHandWritten` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Group Hand Written | Grupo manual |
| 171 | `ReopenOriginalDocument` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reopen Original Document | Reabrir documento original |
| 172 | `ReopenManuallyClosedOrCanceledDocument` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reopen Manually Closed Or Canceled Document | Reabrir documento cerrado manualmente o cancelado |
| 173 | `CreateOnlineQuotation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Create Online Quotation | Crear oferta en línea |
| 174 | `POSEquipmentNumber` | Edm.String | Yes | POS Equipment Number | Número de equipo POS |
| 175 | `POSManufacturerSerialNumber` | Edm.String | Yes | POS Manufacturer Serial Number | Número de serie del fabricante del POS |
| 176 | `POSCashierNumber` | Edm.Int32 | Yes | POS Cashier Number | Número de cajero POS |
| 177 | `ApplyCurrentVATRatesForDownPaymentsToDraw` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Apply Current VAT Rates For Down Payments To Draw | Aplicar tasas de IVA actuales a anticipos a utilizar |
| 178 | `ClosingOption` | [ClosingOptionEnum](../Enums/ClosingOptionEnum.md) | Yes | Closing Option | Opción de cierre |
| 179 | `SpecifiedClosingDate` | Edm.DateTimeOffset | Yes | Specified Closing Date | Fecha de cierre especificada |
| 180 | `OpenForLandedCosts` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Open For Landed Costs | Abierto para costos de importación |
| 181 | `AuthorizationStatus` | [DocumentAuthorizationStatusEnum](../Enums/DocumentAuthorizationStatusEnum.md) | Yes | Authorization Status | Estado de autorización |
| 182 | `TotalDiscountFC` | Edm.Double | Yes | Total Discount FC (foreign currency) | Descuento total (ME) |
| 183 | `TotalDiscountSC` | Edm.Double | Yes | Total Discount SC (system currency) | Descuento total (moneda del sistema) |
| 184 | `RelevantToGTS` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Relevant To GTS | Relevante para GTS |
| 185 | `BPLName` | Edm.String | Yes | Branch Name | Nombre de la sucursal |
| 186 | `VATRegNum` | Edm.String | Yes | VAT Reg Number | Número de registro de IVA |
| 187 | `AnnualInvoiceDeclarationReference` | Edm.Int32 | Yes | Annual Invoice Declaration Reference | Referencia de declaración anual de facturas |
| 188 | `Supplier` | Edm.String | Yes | Supplier | Proveedor |
| 189 | `Releaser` | Edm.Int32 | Yes | Releaser | Liberador |
| 190 | `Receiver` | Edm.Int32 | Yes | Receiver | Receptor |
| 191 | `BlanketAgreementNumber` | Edm.Int32 | Yes | Blanket Agreement Number | Número de acuerdo global |
| 192 | `IsAlteration` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Alteration | Es modificación |
| 193 | `CancelStatus` | [CancelStatusEnum](../Enums/CancelStatusEnum.md) | Yes | Cancel Status | Estado de cancelación |
| 194 | `AssetValueDate` | Edm.DateTimeOffset | Yes | Asset Value Date | Fecha valor del activo |
| 195 | `Requester` | Edm.String | Yes | Requester | Solicitante |
| 196 | `RequesterName` | Edm.String | Yes | Requester Name | Nombre del solicitante |
| 197 | `RequesterBranch` | Edm.Int32 | Yes | Requester Branch | Sucursal del solicitante |
| 198 | `RequesterDepartment` | Edm.Int32 | Yes | Requester Department | Departamento del solicitante |
| 199 | `RequesterEmail` | Edm.String | Yes | Requester Email | Correo del solicitante |
| 200 | `SendNotification` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Send Notification | Enviar notificación |
| 201 | `ReqType` | Edm.Int32 | Yes | Req Type | Tipo de solicitante (usuario/empleado) |
| 202 | `ReqCode` | Edm.String | Yes | Req Code | Código del solicitante |
| 203 | `InvoicePayment` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Invoice Payment | Pago de factura |
| 204 | `DocumentDelivery` | [DocumentDeliveryTypeEnum](../Enums/DocumentDeliveryTypeEnum.md) | Yes | Document Delivery | Entrega del documento |
| 205 | `AuthorizationCode` | Edm.String | Yes | Authorization Code | Código de autorización |
| 206 | `StartDeliveryDate` | Edm.DateTimeOffset | Yes | Start Delivery Date | Fecha de inicio de entrega |
| 207 | `StartDeliveryTime` | Edm.TimeOfDay | Yes | Start Delivery Time | Hora de inicio de entrega |
| 208 | `EndDeliveryDate` | Edm.DateTimeOffset | Yes | End Delivery Date | Fecha de fin de entrega |
| 209 | `EndDeliveryTime` | Edm.TimeOfDay | Yes | End Delivery Time | Hora de fin de entrega |
| 210 | `VehiclePlate` | Edm.String | Yes | Vehicle Plate | Patente del vehículo |
| 211 | `ATDocumentType` | Edm.String | Yes | AT Document Type | Tipo de documento AT |
| 212 | `ElecCommStatus` | [ElecCommStatusEnum](../Enums/ElecCommStatusEnum.md) | Yes | Elec Comm Status | Estado de comunicación electrónica |
| 213 | `ElecCommMessage` | Edm.String | Yes | Elec Comm Message | Mensaje de comunicación electrónica |
| 214 | `ReuseDocumentNum` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reuse Document Number | Reutilizar número de documento |
| 215 | `ReuseNotaFiscalNum` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reuse Nota Fiscal Number | Reutilizar número de Nota Fiscal |
| 216 | `PrintSEPADirect` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Print SEPA Direct | Imprimir débito directo SEPA |
| 217 | `FiscalDocNum` | Edm.String | Yes | Fiscal Document Number | Número de documento fiscal |
| 218 | `POSDailySummaryNo` | Edm.Int32 | Yes | POS Daily Summary Number | N.º de resumen diario POS |
| 219 | `POSReceiptNo` | Edm.Int32 | Yes | POS Receipt Number | Número de recibo POS |
| 220 | `PointOfIssueCode` | Edm.String | Yes | Point Of Issue Code | Código de punto de emisión |
| 221 | `Letter` | [FolioLetterEnum](../Enums/FolioLetterEnum.md) | Yes | Letter | Carta |
| 222 | `FolioNumberFrom` | Edm.Int32 | Yes | Folio Number From | Número de folio desde |
| 223 | `FolioNumberTo` | Edm.Int32 | Yes | Folio Number To | Número de folio hasta |
| 224 | `InterimType` | [BoInterimDocTypes](../Enums/BoInterimDocTypes.md) | Yes | Interim Type | Tipo transitorio |
| 225 | `RelatedType` | Edm.Int32 | Yes | Related Type | Tipo relacionado |
| 226 | `RelatedEntry` | Edm.Int32 | Yes | Related Entry | Entrada relacionada |
| 227 | `SAPPassport` | Edm.String | Yes | SAP Passport | SAP Passport |
| 228 | `DocumentTaxID` | Edm.String | Yes | Document Tax ID | ID fiscal del documento |
| 229 | `DateOfReportingControlStatementVAT` | Edm.DateTimeOffset | Yes | Date Of Reporting Control Statement VAT | Fecha de informe del control de IVA |
| 230 | `ReportingSectionControlStatementVAT` | Edm.String | Yes | Reporting Section Control Statement VAT | Sección del informe de control de IVA |
| 231 | `ExcludeFromTaxReportControlStatementVAT` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Exclude From Tax Report Control Statement VAT | Excluir del informe de control de IVA |
| 232 | `POS_CashRegister` | Edm.Int32 | Yes | POS Cash Register | Caja registradora POS |
| 233 | `UpdateTime` | Edm.TimeOfDay | Yes | Update Time | Hora de actualización |
| 234 | `CreateQRCodeFrom` | Edm.String | Yes | Create QR Code From | Crear código QR desde |
| 235 | `PriceMode` | [PriceModeDocumentEnum](../Enums/PriceModeDocumentEnum.md) | Yes | Price Mode | Modo de precio (neto/bruto) |
| 236 | `DownPaymentTrasactionID` | Edm.String | Yes | Down Payment Trasaction ID | ID de transacción del anticipo |
| 237 | `OriginalRefNo` | Edm.String | Yes | Original Ref Number | N.º de referencia original |
| 238 | `OriginalRefDate` | Edm.DateTimeOffset | Yes | Original Ref Date | Fecha de referencia original |
| 239 | `Revision` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Revision | Revisión |
| 240 | `GSTTransactionType` | [GSTTransactionTypeEnum](../Enums/GSTTransactionTypeEnum.md) | Yes | GST Transaction Type | Tipo de transacción GST |
| 241 | `OriginalCreditOrDebitNo` | Edm.String | Yes | Original Credit Or Debit Number | Número del crédito/débito original |
| 242 | `OriginalCreditOrDebitDate` | Edm.DateTimeOffset | Yes | Original Credit Or Debit Date | Fecha del crédito/débito original |
| 243 | `ECommerceOperator` | Edm.String | Yes | E Commerce Operator | Operador de comercio electrónico |
| 244 | `ECommerceGSTIN` | Edm.String | Yes | E Commerce GSTIN | GSTIN de comercio electrónico |
| 245 | `TaxInvoiceNo` | Edm.String | Yes | Tax Invoice Number | N.º de factura de impuestos |
| 246 | `TaxInvoiceDate` | Edm.DateTimeOffset | Yes | Tax Invoice Date | Fecha de la factura de impuestos |
| 247 | `ShipFrom` | Edm.String | Yes | Ship From | Enviar desde |
| 248 | `CommissionTrade` | [CommissionTradeTypeEnum](../Enums/CommissionTradeTypeEnum.md) | Yes | Commission Trade | Comisión comercial |
| 249 | `CommissionTradeReturn` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Commission Trade Return | Devolución de comisión comercial |
| 250 | `UseBillToAddrToDetermineTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Bill To Addr To Determine Tax | Usar dirección de facturación para determinar impuestos |
| 251 | `IssuingReason` | Edm.Int32 | Yes | Issuing Reason | Motivo de emisión |
| 252 | `Cig` | Edm.Int32 | Yes | Cig | Código CIG |
| 253 | `Cup` | Edm.Int32 | Yes | Cup | Código CUP |
| 254 | `EDocType` | [EDocTypeEnum](../Enums/EDocTypeEnum.md) | Yes | E Document Type | Tipo de documento electrónico |
| 255 | `FCEAsPaymentMeans` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | FCE As Payment Means | FCE como medio de pago |
| 256 | `PaidToDate` | Edm.Double | Yes | Paid To Date | Pagado hasta la fecha |
| 257 | `PaidToDateFC` | Edm.Double | Yes | Paid To Date FC (foreign currency) | Pagado hasta la fecha (ME) |
| 258 | `PaidToDateSys` | Edm.Double | Yes | Paid To Date (system currency) | Pagado hasta la fecha (moneda del sistema) |
| 259 | `FatherCard` | Edm.String | Yes | Father Card | Socio de negocios consolidador (padre) |
| 260 | `FatherType` | [BoFatherCardTypes](../Enums/BoFatherCardTypes.md) | Yes | Father Type | Tipo de consolidación (pagos/entregas) |
| 261 | `ShipState` | Edm.String | Yes | Ship State | Estado de envío |
| 262 | `ShipPlace` | Edm.String | Yes | Ship Place | Lugar de envío |
| 263 | `CustOffice` | Edm.String | Yes | Cust Office | Oficina de aduanas |
| 264 | `FCI` | Edm.String | Yes | FCI | FCI (ficha de contenido de importación, Brasil) |
| 265 | `AddLegIn` | Edm.String | Yes | Add Leg In | Información legal adicional |
| 266 | `LegTextF` | Edm.Int32 | Yes | Leg Text F | Texto legal (idioma extranjero) |
| 267 | `DANFELgTxt` | Edm.String | Yes | DANFE Lg Txt | Texto legal del DANFE |
| 268 | `DataVersion` | Edm.Int32 | Yes | Data Version | Versión de datos (control de concurrencia) |
| 269 | `LastPageFolioNumber` | Edm.Int32 | Yes | Last Page Folio Number | Número de folio de la última página |
| 270 | `InventoryStatus` | [BoStatus](../Enums/BoStatus.md) | Yes | Inventory Status | Estado de inventario |
| 271 | `PlasticPackagingTaxRelevant` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Plastic Packaging Tax Relevant | Relevante para impuesto a envases plásticos |
| 272 | `NotRelevantForMonthlyInvoice` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Not Relevant For Monthly Invoice | No relevante para factura mensual |
| 273 | `EndAt` | [BoPayTermDueTypes](../Enums/BoPayTermDueTypes.md) | Yes | End At | Finaliza en |
| 274 | `ShipToCodeForReturn` | Edm.String | Yes | Ship To Code For Return | Código de dirección de envío para devolución |
| 275 | `AddressForReturn` | Edm.String | Yes | Address For Return | Dirección para devolución |
| 276 | `U_B1SYS_CAI` | Edm.String | Yes | [AR localization] CAI | [Loc. AR] CAI (Código de Autorización de Impresión) |
| 277 | `U_B1SYS_CAI_DATE` | Edm.DateTimeOffset | Yes | [AR localization] CAI DATE | [Loc. AR] Fecha de vencimiento del CAI |
| 278 | `U_B1SYS_ECM2_LINK` | Edm.Int32 | Yes | [AR localization] ECM 2 LINK | [Loc. AR] Vínculo a comunicación electrónica (ECM) |
| 279 | `Document_ApprovalRequests` | Collection([Document_ApprovalRequest](../Tipos-Complejos/Document_ApprovalRequest.md)) | Yes | Document Approval Requests | Solicitudes de autorización del documento |
| 280 | `DocumentLines` | Collection([DocumentLine](../Tipos-Complejos/DocumentLine.md)) | Yes | Document Lines | Líneas del documento |
| 281 | `EWayBillDetails` | [EWayBillDetails](../Tipos-Complejos/EWayBillDetails.md) | Yes | E Way Bill Details | Detalles de E-Way Bill |
| 282 | `EDeliveryInfo` | [EDeliveryInfo](../Tipos-Complejos/EDeliveryInfo.md) | Yes | E Delivery Information | Información de entrega electrónica |
| 283 | `ElectronicProtocols` | Collection([ElectronicProtocol](../Tipos-Complejos/ElectronicProtocol.md)) | Yes | Electronic Protocols | Protocolos electrónicos |
| 284 | `DocumentAdditionalExpenses` | Collection([DocumentAdditionalExpense](../Tipos-Complejos/DocumentAdditionalExpense.md)) | Yes | Document Additional Expenses | Gastos adicionales del documento |
| 285 | `DocumentDistributedExpenses` | Collection([DocumentDistributedExpense](../Tipos-Complejos/DocumentDistributedExpense.md)) | Yes | Document Distributed Expenses | Gastos distribuidos del documento |
| 286 | `WithholdingTaxDataWTXCollection` | Collection([WithholdingTaxDataWTX](../Tipos-Complejos/WithholdingTaxDataWTX.md)) | Yes | Withholding Tax Data WTX Collection | Colección de datos de retención WTX |
| 287 | `WithholdingTaxDataCollection` | Collection([WithholdingTaxData](../Tipos-Complejos/WithholdingTaxData.md)) | Yes | Withholding Tax Data Collection | Colección de datos de retención |
| 288 | `DocumentPackages` | Collection([DocumentPackage](../Tipos-Complejos/DocumentPackage.md)) | Yes | Document Packages | Paquetes del documento |
| 289 | `DocumentSpecialLines` | Collection([DocumentSpecialLine](../Tipos-Complejos/DocumentSpecialLine.md)) | Yes | Document Special Lines | Líneas especiales del documento (texto/subtotal) |
| 290 | `DocumentInstallments` | Collection([DocumentInstallment](../Tipos-Complejos/DocumentInstallment.md)) | Yes | Document Installments | Cuotas del documento |
| 291 | `DownPaymentsToDraw` | Collection([DownPaymentToDraw](../Tipos-Complejos/DownPaymentToDraw.md)) | Yes | Down Payments To Draw | Anticipos a utilizar |
| 292 | `TaxExtension` | [TaxExtension](../Tipos-Complejos/TaxExtension.md) | Yes | Tax Extension | Extensión de impuestos |
| 293 | `AddressExtension` | [AddressExtension](../Tipos-Complejos/AddressExtension.md) | Yes | Address Extension | Extensión de dirección |
| 294 | `DocumentReferences` | Collection([DocumentReference](../Tipos-Complejos/DocumentReference.md)) | Yes | Document References | Referencias del documento |
| 295 | `DocumentAdditionalIntrastatExpenses` | Collection([DocumentAdditionalIntrastatExpense](../Tipos-Complejos/DocumentAdditionalIntrastatExpense.md)) | Yes | Document Additional Intrastat Expenses | Gastos Intrastat adicionales del documento |
| 296 | `BaseType` | Edm.Int32 | Yes | Base Type | Tipo base (tipo de objeto del documento base) |
| 297 | `BaseEntry` | Edm.Int32 | Yes | Base Entry | Entrada base (DocEntry del documento base) |
| 298 | `IndFinal` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Ind Final | Indicador de consumidor final |
| 299 | `AllocationNumberIL` | Edm.String | Yes | Allocation Number IL | Número de asignación (Israel) |
| 300 | `DigitalPayToAddress` | Edm.String | Yes | Digital Pay To Address | Dirección de pago digital |
| 301 | `DigitalPayments` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Digital Payments | Pagos digitales |
| 302 | `SOIWizardId` | Edm.Int32 | Yes | SOI Wizard ID | ID del asistente SOI |

## Navigation properties (26)

Use `GET /b1s/v2/GoodsReturnRequest(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CardCode → CardCode | Socio de negocios |
| `Currency` | [Currency](../Entidades/Currencies.md) | [Currencies](Currencies.md) | DocCurrency → Code | Moneda |
| `PaymentTermsType` | [PaymentTermsType](../Entidades/PaymentTermsTypes.md) | [PaymentTermsTypes](PaymentTermsTypes.md) | PaymentGroupCode → GroupNumber | Condiciones de pago |
| `SalesPerson` | [SalesPerson](../Entidades/SalesPersons.md) | [SalesPersons](SalesPersons.md) | SalesPersonCode → SalesEmployeeCode | Empleado de ventas |
| `ShippingType` | [ShippingType](../Entidades/ShippingTypes.md) | [ShippingTypes](ShippingTypes.md) | TransportationCode → Code | Clase de expedición |
| `FactoringIndicator` | [FactoringIndicator](../Entidades/FactoringIndicators.md) | [FactoringIndicators](FactoringIndicators.md) | Indicator → IndicatorCode | Indicadores de factoring |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | UserSign → InternalKey | Usuario |
| `Forms1099` | [Forms1099](../Entidades/Forms1099.md) | [Forms1099](Forms1099.md) | Form1099 → FormCode | Formularios 1099 |
| `WizardPaymentMethod` | [WizardPaymentMethod](../Entidades/WizardPaymentMethods.md) | [WizardPaymentMethods](WizardPaymentMethods.md) | PaymentMethod → PaymentMethodCode | Vías de pago del asistente de pagos |
| `PaymentBlock2` | [PaymentBlock](../Entidades/PaymentBlocks.md) | [PaymentBlocks](PaymentBlocks.md) | PaymentBlockEntry → AbsEntry | Bloqueos de pago |
| `CentralBankIndicator2` | [CentralBankIndicator](../Entidades/CentralBankIndicator.md) | [CentralBankIndicator](CentralBankIndicator.md) | CentralBankIndicator → Indicator | Indicador del banco central |
| `Project2` | [Project](../Entidades/Projects.md) | [Projects](Projects.md) | Project → Code | Proyectos |
| `EmployeeInfo` | [EmployeeInfo](../Entidades/EmployeesInfo.md) | [EmployeesInfo](EmployeesInfo.md) | DocumentsOwner → EmployeeID | Empleados |
| `Country` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | PayToBankCountry → Code | País |
| `BusinessPlace` | [BusinessPlace](../Entidades/BusinessPlaces.md) | [BusinessPlaces](BusinessPlaces.md) | BPL_IDAssignedToInvoice → BPLID | Lugar de negocios |
| `UserLanguage` | [UserLanguage](../Entidades/UserLanguages.md) | [UserLanguages](UserLanguages.md) | LanguageCode → Code | Idiomas de usuario |
| `NFModel` | [NFModel](../Entidades/NFModels.md) | [NFModels](NFModels.md) | SequenceModel → AbsEntry | Modelos de Nota Fiscal |
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | ControlAccount → Code | Plan de cuentas (cuentas de mayor) |
| `TaxWebSite` | [TaxWebSite](../Entidades/TaxWebSites.md) | [TaxWebSites](TaxWebSites.md) | ETaxWebSite → AbsEntry | Sitios web de impuestos |
| `Branch` | [Branch](../Entidades/Branches.md) | [Branches](Branches.md) | RequesterBranch → Code | Sucursal |
| `Department` | [Department](../Entidades/Departments.md) | [Departments](Departments.md) | RequesterDepartment → Code | Departamento |
| `POSDailySummary` | [POSDailySummary](../Entidades/POSDailySummary.md) | [POSDailySummary](POSDailySummary.md) | POSDailySummaryNo → AbsEntry | Resumen diario de POS |
| `CIGCode` | [CIGCode](../Entidades/CIGCodes.md) | [CIGCodes](CIGCodes.md) | Cig → AbsEntry | Códigos CIG |
| `CUPCode` | [CUPCode](../Entidades/CUPCodes.md) | [CUPCodes](CUPCodes.md) | Cup → AbsEntry | Códigos CUP |
| `JournalEntry` | [JournalEntry](../Entidades/JournalEntries.md) | [JournalEntries](JournalEntries.md) | TransNum → JdtNum | Asientos contables |
| `LandedCost` | [LandedCost](../Entidades/LandedCosts.md) | — | ImportFileNum → DocEntry | Costos de importación (landed costs) |

## Bound actions (4)

### Close

- **Descripción (ES):** Cerrar
- **Request:** `POST /b1s/v2/GoodsReturnRequest(1)/Close`

### Cancel

- **Descripción (ES):** Cancelar
- **Request:** `POST /b1s/v2/GoodsReturnRequest(1)/Cancel`

### Reopen

- **Descripción (ES):** Reabrir
- **Request:** `POST /b1s/v2/GoodsReturnRequest(1)/Reopen`

### CreateCancellationDocument

- **Descripción (ES):** Crear documento de cancelación
- **Request:** `POST /b1s/v2/GoodsReturnRequest(1)/CreateCancellationDocument`
- **Returns:** [Document](../Entidades/PurchaseQuotations.md)


## Service operations that use this type

- [`CorrectionInvoiceReversalService_ApproveAndAdd`](../Servicios/CorrectionInvoiceReversalService.md#correctioninvoicereversalservice_approveandadd)
- [`CorrectionInvoiceReversalService_ApproveAndUpdate`](../Servicios/CorrectionInvoiceReversalService.md#correctioninvoicereversalservice_approveandupdate)
- [`CorrectionInvoiceReversalService_ExportEWayBill`](../Servicios/CorrectionInvoiceReversalService.md#correctioninvoicereversalservice_exportewaybill)
- [`CorrectionInvoiceReversalService_GetApprovalTemplates`](../Servicios/CorrectionInvoiceReversalService.md#correctioninvoicereversalservice_getapprovaltemplates)
- [`CorrectionInvoiceReversalService_InitData`](../Servicios/CorrectionInvoiceReversalService.md#correctioninvoicereversalservice_initdata)
- [`CorrectionInvoiceService_ApproveAndAdd`](../Servicios/CorrectionInvoiceService.md#correctioninvoiceservice_approveandadd)
- [`CorrectionInvoiceService_ApproveAndUpdate`](../Servicios/CorrectionInvoiceService.md#correctioninvoiceservice_approveandupdate)
- [`CorrectionInvoiceService_ExportEWayBill`](../Servicios/CorrectionInvoiceService.md#correctioninvoiceservice_exportewaybill)
- [`CorrectionInvoiceService_GetApprovalTemplates`](../Servicios/CorrectionInvoiceService.md#correctioninvoiceservice_getapprovaltemplates)
- [`CorrectionInvoiceService_InitData`](../Servicios/CorrectionInvoiceService.md#correctioninvoiceservice_initdata)
- [`CorrectionPurchaseInvoiceReversalService_ApproveAndAdd`](../Servicios/CorrectionPurchaseInvoiceReversalService.md#correctionpurchaseinvoicereversalservice_approveandadd)
- [`CorrectionPurchaseInvoiceReversalService_ApproveAndUpdate`](../Servicios/CorrectionPurchaseInvoiceReversalService.md#correctionpurchaseinvoicereversalservice_approveandupdate)
- [`CorrectionPurchaseInvoiceReversalService_ExportEWayBill`](../Servicios/CorrectionPurchaseInvoiceReversalService.md#correctionpurchaseinvoicereversalservice_exportewaybill)
- [`CorrectionPurchaseInvoiceReversalService_GetApprovalTemplates`](../Servicios/CorrectionPurchaseInvoiceReversalService.md#correctionpurchaseinvoicereversalservice_getapprovaltemplates)
- [`CorrectionPurchaseInvoiceReversalService_InitData`](../Servicios/CorrectionPurchaseInvoiceReversalService.md#correctionpurchaseinvoicereversalservice_initdata)
- [`CorrectionPurchaseInvoiceService_ApproveAndAdd`](../Servicios/CorrectionPurchaseInvoiceService.md#correctionpurchaseinvoiceservice_approveandadd)
- [`CorrectionPurchaseInvoiceService_ApproveAndUpdate`](../Servicios/CorrectionPurchaseInvoiceService.md#correctionpurchaseinvoiceservice_approveandupdate)
- [`CorrectionPurchaseInvoiceService_ExportEWayBill`](../Servicios/CorrectionPurchaseInvoiceService.md#correctionpurchaseinvoiceservice_exportewaybill)
- [`CorrectionPurchaseInvoiceService_GetApprovalTemplates`](../Servicios/CorrectionPurchaseInvoiceService.md#correctionpurchaseinvoiceservice_getapprovaltemplates)
- [`CorrectionPurchaseInvoiceService_InitData`](../Servicios/CorrectionPurchaseInvoiceService.md#correctionpurchaseinvoiceservice_initdata)
- [`CreditNotesService_ApproveAndAdd`](../Servicios/CreditNotesService.md#creditnotesservice_approveandadd)
- [`CreditNotesService_ApproveAndUpdate`](../Servicios/CreditNotesService.md#creditnotesservice_approveandupdate)
- [`CreditNotesService_Cancel2`](../Servicios/CreditNotesService.md#creditnotesservice_cancel2)
- [`CreditNotesService_ExportEWayBill`](../Servicios/CreditNotesService.md#creditnotesservice_exportewaybill)
- [`CreditNotesService_GetApprovalTemplates`](../Servicios/CreditNotesService.md#creditnotesservice_getapprovaltemplates)
- [`CreditNotesService_InitData`](../Servicios/CreditNotesService.md#creditnotesservice_initdata)
- [`CreditNotesService_RequestApproveCancellation`](../Servicios/CreditNotesService.md#creditnotesservice_requestapprovecancellation)
- [`DeliveryNotesService_ApproveAndAdd`](../Servicios/DeliveryNotesService.md#deliverynotesservice_approveandadd)
- [`DeliveryNotesService_ApproveAndUpdate`](../Servicios/DeliveryNotesService.md#deliverynotesservice_approveandupdate)
- [`DeliveryNotesService_Cancel2`](../Servicios/DeliveryNotesService.md#deliverynotesservice_cancel2)
- [`DeliveryNotesService_ExportEWayBill`](../Servicios/DeliveryNotesService.md#deliverynotesservice_exportewaybill)
- [`DeliveryNotesService_GetApprovalTemplates`](../Servicios/DeliveryNotesService.md#deliverynotesservice_getapprovaltemplates)
- [`DeliveryNotesService_InitData`](../Servicios/DeliveryNotesService.md#deliverynotesservice_initdata)
- [`DownPaymentsService_ApproveAndAdd`](../Servicios/DownPaymentsService.md#downpaymentsservice_approveandadd)
- [`DownPaymentsService_ApproveAndUpdate`](../Servicios/DownPaymentsService.md#downpaymentsservice_approveandupdate)
- [`DownPaymentsService_ExportEWayBill`](../Servicios/DownPaymentsService.md#downpaymentsservice_exportewaybill)
- [`DownPaymentsService_GetApprovalTemplates`](../Servicios/DownPaymentsService.md#downpaymentsservice_getapprovaltemplates)
- [`DownPaymentsService_InitData`](../Servicios/DownPaymentsService.md#downpaymentsservice_initdata)
- [`DraftsService_ApproveAndAdd`](../Servicios/DraftsService.md#draftsservice_approveandadd)
- [`DraftsService_ApproveAndUpdate`](../Servicios/DraftsService.md#draftsservice_approveandupdate)
- [`DraftsService_ExportEWayBill`](../Servicios/DraftsService.md#draftsservice_exportewaybill)
- [`DraftsService_GetApprovalTemplates`](../Servicios/DraftsService.md#draftsservice_getapprovaltemplates)
- [`DraftsService_InitData`](../Servicios/DraftsService.md#draftsservice_initdata)
- [`DraftsService_SaveDraftToDocument`](../Servicios/DraftsService.md#draftsservice_savedrafttodocument)
- [`GoodsReturnRequestService_ApproveAndAdd`](../Servicios/GoodsReturnRequestService.md#goodsreturnrequestservice_approveandadd)
- [`GoodsReturnRequestService_ApproveAndUpdate`](../Servicios/GoodsReturnRequestService.md#goodsreturnrequestservice_approveandupdate)
- [`GoodsReturnRequestService_ExportEWayBill`](../Servicios/GoodsReturnRequestService.md#goodsreturnrequestservice_exportewaybill)
- [`GoodsReturnRequestService_GetApprovalTemplates`](../Servicios/GoodsReturnRequestService.md#goodsreturnrequestservice_getapprovaltemplates)
- [`GoodsReturnRequestService_InitData`](../Servicios/GoodsReturnRequestService.md#goodsreturnrequestservice_initdata)
- [`InventoryGenEntryService_ApproveAndAdd`](../Servicios/InventoryGenEntryService.md#inventorygenentryservice_approveandadd)
- [`InventoryGenEntryService_ApproveAndUpdate`](../Servicios/InventoryGenEntryService.md#inventorygenentryservice_approveandupdate)
- [`InventoryGenEntryService_ExportEWayBill`](../Servicios/InventoryGenEntryService.md#inventorygenentryservice_exportewaybill)
- [`InventoryGenEntryService_GetApprovalTemplates`](../Servicios/InventoryGenEntryService.md#inventorygenentryservice_getapprovaltemplates)
- [`InventoryGenEntryService_InitData`](../Servicios/InventoryGenEntryService.md#inventorygenentryservice_initdata)
- [`InventoryGenExitService_ApproveAndAdd`](../Servicios/InventoryGenExitService.md#inventorygenexitservice_approveandadd)
- [`InventoryGenExitService_ApproveAndUpdate`](../Servicios/InventoryGenExitService.md#inventorygenexitservice_approveandupdate)
- [`InventoryGenExitService_ExportEWayBill`](../Servicios/InventoryGenExitService.md#inventorygenexitservice_exportewaybill)
- [`InventoryGenExitService_GetApprovalTemplates`](../Servicios/InventoryGenExitService.md#inventorygenexitservice_getapprovaltemplates)
- [`InventoryGenExitService_InitData`](../Servicios/InventoryGenExitService.md#inventorygenexitservice_initdata)
- [`InvoicesService_ApproveAndAdd`](../Servicios/InvoicesService.md#invoicesservice_approveandadd)
- [`InvoicesService_ApproveAndUpdate`](../Servicios/InvoicesService.md#invoicesservice_approveandupdate)
- [`InvoicesService_Cancel2`](../Servicios/InvoicesService.md#invoicesservice_cancel2)
- [`InvoicesService_ExportEWayBill`](../Servicios/InvoicesService.md#invoicesservice_exportewaybill)
- [`InvoicesService_GetApprovalTemplates`](../Servicios/InvoicesService.md#invoicesservice_getapprovaltemplates)
- [`InvoicesService_InitData`](../Servicios/InvoicesService.md#invoicesservice_initdata)
- [`InvoicesService_RequestApproveCancellation`](../Servicios/InvoicesService.md#invoicesservice_requestapprovecancellation)
- [`OrdersService_ApproveAndAdd`](../Servicios/OrdersService.md#ordersservice_approveandadd)
- [`OrdersService_ApproveAndUpdate`](../Servicios/OrdersService.md#ordersservice_approveandupdate)
- [`OrdersService_ExportEWayBill`](../Servicios/OrdersService.md#ordersservice_exportewaybill)
- [`OrdersService_GetApprovalTemplates`](../Servicios/OrdersService.md#ordersservice_getapprovaltemplates)
- [`OrdersService_InitData`](../Servicios/OrdersService.md#ordersservice_initdata)
- [`OrdersService_Preview`](../Servicios/OrdersService.md#ordersservice_preview)
- [`PurchaseCreditNotesService_ApproveAndAdd`](../Servicios/PurchaseCreditNotesService.md#purchasecreditnotesservice_approveandadd)
- [`PurchaseCreditNotesService_ApproveAndUpdate`](../Servicios/PurchaseCreditNotesService.md#purchasecreditnotesservice_approveandupdate)
- [`PurchaseCreditNotesService_Cancel2`](../Servicios/PurchaseCreditNotesService.md#purchasecreditnotesservice_cancel2)
- [`PurchaseCreditNotesService_ExportEWayBill`](../Servicios/PurchaseCreditNotesService.md#purchasecreditnotesservice_exportewaybill)
- [`PurchaseCreditNotesService_GetApprovalTemplates`](../Servicios/PurchaseCreditNotesService.md#purchasecreditnotesservice_getapprovaltemplates)
- [`PurchaseCreditNotesService_InitData`](../Servicios/PurchaseCreditNotesService.md#purchasecreditnotesservice_initdata)
- [`PurchaseDeliveryNotesService_ApproveAndAdd`](../Servicios/PurchaseDeliveryNotesService.md#purchasedeliverynotesservice_approveandadd)
- [`PurchaseDeliveryNotesService_ApproveAndUpdate`](../Servicios/PurchaseDeliveryNotesService.md#purchasedeliverynotesservice_approveandupdate)
- [`PurchaseDeliveryNotesService_Cancel2`](../Servicios/PurchaseDeliveryNotesService.md#purchasedeliverynotesservice_cancel2)
- [`PurchaseDeliveryNotesService_ExportEWayBill`](../Servicios/PurchaseDeliveryNotesService.md#purchasedeliverynotesservice_exportewaybill)
- [`PurchaseDeliveryNotesService_GetApprovalTemplates`](../Servicios/PurchaseDeliveryNotesService.md#purchasedeliverynotesservice_getapprovaltemplates)
- [`PurchaseDeliveryNotesService_InitData`](../Servicios/PurchaseDeliveryNotesService.md#purchasedeliverynotesservice_initdata)
- [`PurchaseDownPaymentsService_ApproveAndAdd`](../Servicios/PurchaseDownPaymentsService.md#purchasedownpaymentsservice_approveandadd)
- [`PurchaseDownPaymentsService_ApproveAndUpdate`](../Servicios/PurchaseDownPaymentsService.md#purchasedownpaymentsservice_approveandupdate)
- [`PurchaseDownPaymentsService_ExportEWayBill`](../Servicios/PurchaseDownPaymentsService.md#purchasedownpaymentsservice_exportewaybill)
- [`PurchaseDownPaymentsService_GetApprovalTemplates`](../Servicios/PurchaseDownPaymentsService.md#purchasedownpaymentsservice_getapprovaltemplates)
- [`PurchaseDownPaymentsService_InitData`](../Servicios/PurchaseDownPaymentsService.md#purchasedownpaymentsservice_initdata)
- [`PurchaseInvoicesService_ApproveAndAdd`](../Servicios/PurchaseInvoicesService.md#purchaseinvoicesservice_approveandadd)
- [`PurchaseInvoicesService_ApproveAndUpdate`](../Servicios/PurchaseInvoicesService.md#purchaseinvoicesservice_approveandupdate)
- [`PurchaseInvoicesService_Cancel2`](../Servicios/PurchaseInvoicesService.md#purchaseinvoicesservice_cancel2)
- [`PurchaseInvoicesService_ExportEWayBill`](../Servicios/PurchaseInvoicesService.md#purchaseinvoicesservice_exportewaybill)
- [`PurchaseInvoicesService_GetApprovalTemplates`](../Servicios/PurchaseInvoicesService.md#purchaseinvoicesservice_getapprovaltemplates)
- [`PurchaseInvoicesService_InitData`](../Servicios/PurchaseInvoicesService.md#purchaseinvoicesservice_initdata)
- [`PurchaseOrdersService_ApproveAndAdd`](../Servicios/PurchaseOrdersService.md#purchaseordersservice_approveandadd)
- [`PurchaseOrdersService_ApproveAndUpdate`](../Servicios/PurchaseOrdersService.md#purchaseordersservice_approveandupdate)
- [`PurchaseOrdersService_ExportEWayBill`](../Servicios/PurchaseOrdersService.md#purchaseordersservice_exportewaybill)
- [`PurchaseOrdersService_GetApprovalTemplates`](../Servicios/PurchaseOrdersService.md#purchaseordersservice_getapprovaltemplates)
- [`PurchaseOrdersService_InitData`](../Servicios/PurchaseOrdersService.md#purchaseordersservice_initdata)
- [`PurchaseQuotationsService_ApproveAndAdd`](../Servicios/PurchaseQuotationsService.md#purchasequotationsservice_approveandadd)
- [`PurchaseQuotationsService_ApproveAndUpdate`](../Servicios/PurchaseQuotationsService.md#purchasequotationsservice_approveandupdate)
- [`PurchaseQuotationsService_ExportEWayBill`](../Servicios/PurchaseQuotationsService.md#purchasequotationsservice_exportewaybill)
- [`PurchaseQuotationsService_GetApprovalTemplates`](../Servicios/PurchaseQuotationsService.md#purchasequotationsservice_getapprovaltemplates)
- [`PurchaseQuotationsService_InitData`](../Servicios/PurchaseQuotationsService.md#purchasequotationsservice_initdata)
- [`PurchaseRequestService_ApproveAndAdd`](../Servicios/PurchaseRequestService.md#purchaserequestservice_approveandadd)
- [`PurchaseRequestService_ApproveAndUpdate`](../Servicios/PurchaseRequestService.md#purchaserequestservice_approveandupdate)
- [`PurchaseRequestService_ExportEWayBill`](../Servicios/PurchaseRequestService.md#purchaserequestservice_exportewaybill)
- [`PurchaseRequestService_GetApprovalTemplates`](../Servicios/PurchaseRequestService.md#purchaserequestservice_getapprovaltemplates)
- [`PurchaseRequestService_InitData`](../Servicios/PurchaseRequestService.md#purchaserequestservice_initdata)
- [`PurchaseReturnsService_ApproveAndAdd`](../Servicios/PurchaseReturnsService.md#purchasereturnsservice_approveandadd)
- [`PurchaseReturnsService_ApproveAndUpdate`](../Servicios/PurchaseReturnsService.md#purchasereturnsservice_approveandupdate)
- [`PurchaseReturnsService_Cancel2`](../Servicios/PurchaseReturnsService.md#purchasereturnsservice_cancel2)
- [`PurchaseReturnsService_ExportEWayBill`](../Servicios/PurchaseReturnsService.md#purchasereturnsservice_exportewaybill)
- [`PurchaseReturnsService_GetApprovalTemplates`](../Servicios/PurchaseReturnsService.md#purchasereturnsservice_getapprovaltemplates)
- [`PurchaseReturnsService_InitData`](../Servicios/PurchaseReturnsService.md#purchasereturnsservice_initdata)
- [`QuotationsService_ApproveAndAdd`](../Servicios/QuotationsService.md#quotationsservice_approveandadd)
- [`QuotationsService_ApproveAndUpdate`](../Servicios/QuotationsService.md#quotationsservice_approveandupdate)
- [`QuotationsService_ExportEWayBill`](../Servicios/QuotationsService.md#quotationsservice_exportewaybill)
- [`QuotationsService_GetApprovalTemplates`](../Servicios/QuotationsService.md#quotationsservice_getapprovaltemplates)
- [`QuotationsService_InitData`](../Servicios/QuotationsService.md#quotationsservice_initdata)
- [`ReturnRequestService_ApproveAndAdd`](../Servicios/ReturnRequestService.md#returnrequestservice_approveandadd)
- [`ReturnRequestService_ApproveAndUpdate`](../Servicios/ReturnRequestService.md#returnrequestservice_approveandupdate)
- [`ReturnRequestService_ExportEWayBill`](../Servicios/ReturnRequestService.md#returnrequestservice_exportewaybill)
- [`ReturnRequestService_GetApprovalTemplates`](../Servicios/ReturnRequestService.md#returnrequestservice_getapprovaltemplates)
- [`ReturnRequestService_InitData`](../Servicios/ReturnRequestService.md#returnrequestservice_initdata)
- [`ReturnsService_ApproveAndAdd`](../Servicios/ReturnsService.md#returnsservice_approveandadd)
- [`ReturnsService_ApproveAndUpdate`](../Servicios/ReturnsService.md#returnsservice_approveandupdate)
- [`ReturnsService_Cancel2`](../Servicios/ReturnsService.md#returnsservice_cancel2)
- [`ReturnsService_ExportEWayBill`](../Servicios/ReturnsService.md#returnsservice_exportewaybill)
- [`ReturnsService_GetApprovalTemplates`](../Servicios/ReturnsService.md#returnsservice_getapprovaltemplates)
- [`ReturnsService_InitData`](../Servicios/ReturnsService.md#returnsservice_initdata)
- [`SelfCreditMemoService_ApproveAndAdd`](../Servicios/SelfCreditMemoService.md#selfcreditmemoservice_approveandadd)
- [`SelfCreditMemoService_ApproveAndUpdate`](../Servicios/SelfCreditMemoService.md#selfcreditmemoservice_approveandupdate)
- [`SelfCreditMemoService_ExportEWayBill`](../Servicios/SelfCreditMemoService.md#selfcreditmemoservice_exportewaybill)
- [`SelfCreditMemoService_GetApprovalTemplates`](../Servicios/SelfCreditMemoService.md#selfcreditmemoservice_getapprovaltemplates)
- [`SelfCreditMemoService_InitData`](../Servicios/SelfCreditMemoService.md#selfcreditmemoservice_initdata)
- [`SelfInvoiceService_ApproveAndAdd`](../Servicios/SelfInvoiceService.md#selfinvoiceservice_approveandadd)
- [`SelfInvoiceService_ApproveAndUpdate`](../Servicios/SelfInvoiceService.md#selfinvoiceservice_approveandupdate)
- [`SelfInvoiceService_ExportEWayBill`](../Servicios/SelfInvoiceService.md#selfinvoiceservice_exportewaybill)
- [`SelfInvoiceService_GetApprovalTemplates`](../Servicios/SelfInvoiceService.md#selfinvoiceservice_getapprovaltemplates)
- [`SelfInvoiceService_InitData`](../Servicios/SelfInvoiceService.md#selfinvoiceservice_initdata)
