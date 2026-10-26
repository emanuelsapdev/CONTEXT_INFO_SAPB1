# ElectronicProtocol — Protocolos electrónicos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ElectronicProtocol`
- **Descripción (ES):** Protocolos electrónicos
- **Description (EN):** Electronic Protocol
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 40

## Properties (40)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ProtocolCode` | [ElectronicDocProtocolCodeEnum](../Enums/ElectronicDocProtocolCodeEnum.md) | Yes | Protocol Code | Código de protocolo |
| 2 | `GenerationType` | [ElectronicDocGenTypeEnum](../Enums/ElectronicDocGenTypeEnum.md) | Yes | Generation Type | Tipo de generación |
| 3 | `MappingID` | Edm.Int32 | Yes | Mapping ID | ID de mapeo |
| 4 | `TestingMode` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Testing Mode | Modo de prueba |
| 5 | `Confirmation` | Edm.String | Yes | Confirmation | Confirmación |
| 6 | `EDocType` | Edm.Int32 | Yes | E Document Type | Tipo de documento electrónico |
| 7 | `CFDiCancellationReason` | Edm.String | Yes | CF Di Cancellation Reason | Motivo de cancelación de CFDI (México) |
| 8 | `CFDiCancellationResponse` | Edm.String | Yes | CF Di Cancellation Response | Respuesta de cancelación de CFDI |
| 9 | `RelatedDocuments` | Collection([RelatedDocument](../Tipos-Complejos/RelatedDocument.md)) | Yes | Related Documents | Documentos relacionados |
| 10 | `EBooksRelevant` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | E Books Relevant | Relevante para libros electrónicos |
| 11 | `EBooksMARK` | Edm.String | Yes | E Books MARK | MARK de libros electrónicos (Grecia) |
| 12 | `EBooksMARKofNegative` | Edm.String | Yes | E Books MAR Kof Negative | MARK negativo de libros electrónicos |
| 13 | `EBooksInvoiceType` | Edm.String | Yes | E Books Invoice Type | Tipo de factura (libros electrónicos) |
| 14 | `EBooksInvoiceTypeofNegative` | Edm.String | Yes | E Books Invoice Typeof Negative | Tipo de factura negativa (libros electrónicos) |
| 15 | `EBillingIRN` | Edm.String | Yes | E Billing IRN | IRN de facturación electrónica |
| 16 | `EETPKP` | Edm.String | Yes | EETPKP | Código PKP de EET (Rep. Checa) |
| 17 | `EETBKP` | Edm.String | Yes | EETBKP | Código BKP de EET (Rep. Checa) |
| 18 | `SignatureInputMessage` | Edm.String | Yes | Signature Input Message | Mensaje de entrada de la firma |
| 19 | `SignatureDigest` | Edm.String | Yes | Signature Digest | Resumen de firma |
| 20 | `FechaTimbrado` | Edm.String | Yes | Fecha Timbrado | Fecha de timbrado (México) |
| 21 | `SelloSAT` | Edm.String | Yes | Sello SAT | Sello SAT (México) |
| 22 | `PaymentMethod` | Edm.String | Yes | Payment Method | Vía de pago |
| 23 | `RfcProvCertif` | Edm.String | Yes | Rfc Prov Certif | RFC del proveedor de certificación (México) |
| 24 | `NoCertificadoSAT` | Edm.String | Yes | Number Certificado SAT | N.º de certificado SAT (México) |
| 25 | `FPASequenceNumber` | Edm.Int32 | Yes | FPA Sequence Number | Número de secuencia FPA (Italia) |
| 26 | `FPASendDateSDI` | Edm.DateTimeOffset | Yes | FPA Send Date SDI | Fecha de envío al SDI (Italia) |
| 27 | `FPAProgressivo` | Edm.String | Yes | FPA Progressivo | Progresivo de factura electrónica (Italia) |
| 28 | `ProtocolDescription` | Edm.String | Yes | Protocol Description | Descripción del protocolo |
| 29 | `CFDiExport` | Edm.String | Yes | CF Di Export | Exportación CFDI |
| 30 | `EBillingAckNo` | Edm.String | Yes | E Billing Ack Number | N.º de acuse de facturación electrónica |
| 31 | `EBillingAckDt` | Edm.String | Yes | E Billing Ack Dt | Fecha de acuse de facturación electrónica (India) |
| 32 | `EBillingSignedInvoice` | Edm.String | Yes | E Billing Signed Invoice | Factura firmada de facturación electrónica |
| 33 | `EBillingSignedQRCode` | Edm.String | Yes | E Billing Signed QR Code | Código QR firmado de facturación electrónica |
| 34 | `EBillingResponseStatus` | Edm.String | Yes | E Billing Response Status | Estado de respuesta de facturación electrónica |
| 35 | `CFDiCancellationReference` | Edm.String | Yes | CF Di Cancellation Reference | Referencia de cancelación de CFDI |
| 36 | `EBooksQRCodePath` | Edm.String | Yes | E Books QR Code Path | Ruta del código QR (libros electrónicos) |
| 37 | `EBooksQRCodePathofNegative` | Edm.String | Yes | E Books QR Code Pathof Negative | Ruta del código QR negativo |
| 38 | `CartaPorteID` | Edm.String | Yes | Carta Porte ID | ID de Carta Porte (México) |
| 39 | `EBooksDispatchDate` | Edm.DateTimeOffset | Yes | E Books Dispatch Date | Fecha de despacho (libros electrónicos) |
| 40 | `EBooksDispatchTime` | Edm.TimeOfDay | Yes | E Books Dispatch Time | Hora de despacho (libros electrónicos) |

## Used by (properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`ElectronicProtocols`
- [Document](../Entidades/PurchaseQuotations.md).`ElectronicProtocols`
- [InternalReconciliation](../Entidades/InternalReconciliations.md).`ElectronicProtocols`
- [InternalReconciliationOpenTrans](InternalReconciliationOpenTrans.md).`ElectronicProtocols`
- [JournalEntry](../Entidades/JournalEntries.md).`ElectronicProtocols`
- [Payment](../Entidades/VendorPayments.md).`ElectronicProtocols`
- [StockTransfer](../Entidades/StockTransfers.md).`ElectronicProtocols`
- [TransportationDocumentData](../Entidades/TransportationDocument.md).`ElectronicProtocols`
