# Currencies — Monedas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Currencies`
- **Descripción (ES):** Monedas
- **Entity type:** `Currency` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OCRN](../../Tablas%20SAP%20B1/OCRN.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 18 · **Navigation properties:** 39 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Currencies?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Currencies/$count` | Contar |
| Get by key | `GET /b1s/v2/Currencies('value')` | Obtener por clave |
| Create | `POST /b1s/v2/Currencies` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Currencies('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Currencies('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/Currencies('value')` (only if the B1 object allows removal) | Borrar |

## Properties (18)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `DocumentsCode` | Edm.String | Yes | Documents Code | Código de documentos |
| 4 | `InternationalDescription` | Edm.String | Yes | International Description | Descripción internacional |
| 5 | `HundredthName` | Edm.String | Yes | Hundredth Name | Nombre de centésimos |
| 6 | `EnglishName` | Edm.String | Yes | English Name | Nombre en inglés |
| 7 | `EnglishHundredthName` | Edm.String | Yes | English Hundredth Name | Nombre de centésimos en inglés |
| 8 | `PluralInternationalDescription` | Edm.String | Yes | Plural International Description | Descripción internacional plural |
| 9 | `PluralHundredthName` | Edm.String | Yes | Plural Hundredth Name | Nombre plural de centésimos |
| 10 | `PluralEnglishName` | Edm.String | Yes | Plural English Name | Nombre plural en inglés |
| 11 | `PluralEnglishHundredthName` | Edm.String | Yes | Plural English Hundredth Name | Nombre plural de centésimos en inglés |
| 12 | `Decimals` | [CurrenciesDecimalsEnum](../Enums/CurrenciesDecimalsEnum.md) | Yes | Decimals | Decimales |
| 13 | `Rounding` | [RoundingSysEnum](../Enums/RoundingSysEnum.md) | Yes | Rounding | Redondeo |
| 14 | `RoundingInPayment` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Rounding In Payment | Redondeo en el pago |
| 15 | `MaxIncomingAmtDiff` | Edm.Double | Yes | Max Incoming Amount Diff | Diferencia máxima de importe en cobros |
| 16 | `MaxOutgoingAmtDiff` | Edm.Double | Yes | Max Outgoing Amount Diff | Diferencia máxima de importe en pagos |
| 17 | `MaxIncomingAmtDiffPercent` | Edm.Double | Yes | Max Incoming Amount Diff Percent | Porcentaje de diferencia máxima en cobros |
| 18 | `MaxOutgoingAmtDiffPercent` | Edm.Double | Yes | Max Outgoing Amount Diff Percent | Porcentaje de diferencia máxima en pagos |

## Navigation properties (39)

Use `GET /b1s/v2/Currencies('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `PurchaseQuotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseQuotations](PurchaseQuotations.md) |  | Ofertas de compra |
| `VendorPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [VendorPayments](VendorPayments.md) |  | Pagos efectuados |
| `CorrectionInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoiceReversal](CorrectionInvoiceReversal.md) |  | Anulación de factura de corrección de clientes |
| `CorrectionInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoice](CorrectionInvoice.md) |  | Factura de corrección de clientes |
| `WithholdingTaxCodes` | Collection([WithholdingTaxCode](../Entidades/WithholdingTaxCodes.md)) | [WithholdingTaxCodes](WithholdingTaxCodes.md) |  | Códigos de retención de impuestos |
| `PurchaseDeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDeliveryNotes](PurchaseDeliveryNotes.md) |  | Pedidos de entrada de mercancías |
| `CorrectionPurchaseInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoice](CorrectionPurchaseInvoice.md) |  | Factura de corrección de proveedores |
| `InventoryGenEntries` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenEntries](InventoryGenEntries.md) |  | Entradas de mercancías |
| `AssetRetirement` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetRetirement](AssetRetirement.md) |  | Baja de activos |
| `AssetTransfer` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetTransfer](AssetTransfer.md) |  | Transferencia de activos |
| `AssetManualDepreciation` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetManualDepreciation](AssetManualDepreciation.md) |  | Amortización manual de activos |
| `Orders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Orders](Orders.md) |  | Pedidos de cliente (órdenes de venta) |
| `AssetCapitalization` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetCapitalization](AssetCapitalization.md) |  | Capitalización de activos fijos |
| `InventoryGenExits` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenExits](InventoryGenExits.md) |  | Salidas de mercancías |
| `Drafts` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Drafts](Drafts.md) |  | Borradores de documentos |
| `ChartOfAccounts` | Collection([ChartOfAccount](../Entidades/ChartOfAccounts.md)) | [ChartOfAccounts](ChartOfAccounts.md) |  | Plan de cuentas (cuentas de mayor) |
| `ReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [ReturnRequest](ReturnRequest.md) |  | Solicitudes de devolución de clientes |
| `DeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DeliveryNotes](DeliveryNotes.md) |  | Entregas |
| `BankStatements` | Collection([BankStatement](../Entidades/BankStatements.md)) | [BankStatements](BankStatements.md) |  | Extractos bancarios |
| `PurchaseInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseInvoices](PurchaseInvoices.md) |  | Facturas de proveedores |
| `SelfInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfInvoices](SelfInvoices.md) |  | Autofacturas |
| `BlanketAgreements` | Collection([BlanketAgreement](../Entidades/BlanketAgreements.md)) | [BlanketAgreements](BlanketAgreements.md) |  | Acuerdos globales |
| `Invoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Invoices](Invoices.md) |  | Facturas de clientes |
| `CreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CreditNotes](CreditNotes.md) |  | Notas de crédito de clientes |
| `AssetCapitalizationCreditMemo` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetCapitalizationCreditMemo](AssetCapitalizationCreditMemo.md) |  | Nota de crédito de capitalización de activos |
| `PaymentDrafts` | Collection([Payment](../Entidades/VendorPayments.md)) | [PaymentDrafts](PaymentDrafts.md) |  | Borradores de pagos |
| `PurchaseCreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseCreditNotes](PurchaseCreditNotes.md) |  | Notas de crédito de proveedores |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
| `DownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DownPayments](DownPayments.md) |  | Facturas de anticipo de clientes |
| `PurchaseDownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDownPayments](PurchaseDownPayments.md) |  | Facturas de anticipo de proveedores |
| `PurchaseReturns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseReturns](PurchaseReturns.md) |  | Devoluciones de mercancías a proveedores |
| `PurchaseOrders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseOrders](PurchaseOrders.md) |  | Pedidos de compra (órdenes de compra) |
| `SelfCreditMemos` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfCreditMemos](SelfCreditMemos.md) |  | Autonotas de crédito |
| `Quotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Quotations](Quotations.md) |  | Ofertas de ventas (cotizaciones) |
| `Returns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Returns](Returns.md) |  | Devoluciones de clientes |
| `GoodsReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [GoodsReturnRequest](GoodsReturnRequest.md) |  | Solicitudes de devolución de mercancías |
| `CorrectionPurchaseInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoiceReversal](CorrectionPurchaseInvoiceReversal.md) |  | Anulación de factura de corrección de proveedores |
| `IncomingPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [IncomingPayments](IncomingPayments.md) |  | Pagos recibidos |
| `PurchaseRequests` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseRequests](PurchaseRequests.md) |  | Solicitudes de compra |
