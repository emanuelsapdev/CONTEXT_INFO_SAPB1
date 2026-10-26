# BusinessPlaces — Lugares de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BusinessPlaces`
- **Descripción (ES):** Lugares de negocios
- **Entity type:** `BusinessPlace` (open type: accepts dynamic/UDF properties)
- **Key:** `BPLID` (Edm.Int32)
- **DB tables (main / lines):** [ABPL](../../Tablas%20SAP%20B1/ABPL.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 51 · **Navigation properties:** 54 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BusinessPlaces?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BusinessPlaces/$count` | Contar |
| Get by key | `GET /b1s/v2/BusinessPlaces(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BusinessPlaces` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BusinessPlaces(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BusinessPlaces(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BusinessPlaces(1)` (only if the B1 object allows removal) | Borrar |

## Properties (51)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BPLID` 🔑 | Edm.Int32 | No | BPLID | ID de sucursal |
| 2 | `BPLName` | Edm.String | Yes | Branch Name | Nombre de la sucursal |
| 3 | `BPLNameForeign` | Edm.String | Yes | Branch Name Foreign | Nombre extranjero de la sucursal |
| 4 | `VATRegNum` | Edm.String | Yes | VAT Reg Number | Número de registro de IVA |
| 5 | `RepName` | Edm.String | Yes | Rep Name | Nombre del informe |
| 6 | `Industry` | Edm.String | Yes | Industry | Ramo (industria) |
| 7 | `Business` | Edm.String | Yes | Business | Negocio |
| 8 | `Address` | Edm.String | Yes | Address | Dirección |
| 9 | `Addressforeign` | Edm.String | Yes | Addressforeign | Dirección en idioma extranjero |
| 10 | `MainBPL` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Main Branch | Sucursal principal |
| 11 | `TaxOfficeNo` | Edm.String | Yes | Tax Office Number | N.º de oficina tributaria |
| 12 | `Disabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Disabled | Deshabilitado |
| 13 | `DefaultCustomerID` | Edm.String | Yes | Default Customer ID | ID de cliente predeterminado |
| 14 | `DefaultVendorID` | Edm.String | Yes | Default Vendor ID | ID de proveedor predeterminado |
| 15 | `DefaultWarehouseID` | Edm.String | Yes | Default Warehouse ID | ID de almacén predeterminado |
| 16 | `DefaultTaxCode` | Edm.String | Yes | Default Tax Code | Indicador de impuesto predeterminado |
| 17 | `TaxOffice` | Edm.String | Yes | Tax Office | Oficina tributaria |
| 18 | `FederalTaxID` | Edm.String | Yes | Federal Tax ID | CUIT / ID fiscal federal |
| 19 | `FederalTaxID2` | Edm.String | Yes | Federal Tax ID 2 | ID fiscal federal 2 |
| 20 | `FederalTaxID3` | Edm.String | Yes | Federal Tax ID 3 | ID fiscal federal 3 |
| 21 | `AdditionalIdNumber` | Edm.String | Yes | Additional ID Number | Número de identificación adicional |
| 22 | `NatureOfCompanyCode` | Edm.Int32 | Yes | Nature Of Company Code | Código de naturaleza de la sociedad |
| 23 | `EconomicActivityTypeCode` | Edm.Int32 | Yes | Economic Activity Type Code | Código de tipo de actividad económica |
| 24 | `CreditContributionOriginCode` | Edm.String | Yes | Credit Contribution Origin Code | Código de origen de crédito de contribución |
| 25 | `IPIPeriodCode` | Edm.String | Yes | IPI Period Code | Código de período IPI |
| 26 | `CooperativeAssociationTypeCode` | Edm.Int32 | Yes | Cooperative Association Type Code | Código de tipo de asociación cooperativa |
| 27 | `ProfitTaxationCode` | Edm.Int32 | Yes | Profit Taxation Code | Código de tributación de beneficios |
| 28 | `CompanyQualificationCode` | Edm.Int32 | Yes | Company Qualification Code | Código de calificación de la sociedad |
| 29 | `DeclarerTypeCode` | Edm.Int32 | Yes | Declarer Type Code | Código de tipo de declarante |
| 30 | `PreferredStateCode` | Edm.String | Yes | Preferred State Code | Código de estado preferido |
| 31 | `AddressType` | Edm.String | Yes | Address Type | Tipo de dirección |
| 32 | `Street` | Edm.String | Yes | Street | Calle |
| 33 | `StreetNo` | Edm.String | Yes | Street Number | Número de calle |
| 34 | `Building` | Edm.String | Yes | Building | Edificio |
| 35 | `ZipCode` | Edm.String | Yes | Zip Code | Código postal |
| 36 | `Block` | Edm.String | Yes | Block | Barrio/bloque |
| 37 | `City` | Edm.String | Yes | City | Ciudad |
| 38 | `State` | Edm.String | Yes | State | Estado/provincia |
| 39 | `County` | Edm.String | Yes | County | Condado |
| 40 | `Country` | Edm.String | Yes | Country | País |
| 41 | `AliasName` | Edm.String | Yes | Alias Name | Alias |
| 42 | `CommercialRegister` | Edm.String | Yes | Commercial Register | Registro comercial |
| 43 | `DateOfIncorporation` | Edm.DateTimeOffset | Yes | Date Of Incorporation | Fecha de constitución |
| 44 | `SPEDProfile` | Edm.String | Yes | SPED Profile | Perfil SPED (Brasil) |
| 45 | `EnvironmentType` | Edm.Int32 | Yes | Environment Type | Tipo de entorno |
| 46 | `Opting4ICMS` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Opting 4 ICMS | Opción por ICMS |
| 47 | `PaymentClearingAccount` | Edm.String | Yes | Payment Clearing Account | Cuenta de compensación de pagos |
| 48 | `GlobalLocationNumber` | Edm.String | Yes | Global Location Number | Número de localización global (GLN) |
| 49 | `DefaultResourceWarehouseID` | Edm.String | Yes | Default Resource Warehouse ID | Almacén de recursos predeterminado |
| 50 | `BusinessPlaceIENumbers` | Collection([BusinessPlaceIENumber](../Tipos-Complejos/BusinessPlaceIENumber.md)) | Yes | Business Place IE Numbers | Números de I.E. del lugar de negocios |
| 51 | `BusinessPlaceTributaryInfos` | Collection([BusinessPlaceTributaryInfo](../Tipos-Complejos/BusinessPlaceTributaryInfo.md)) | Yes | Business Place Tributary Infos | Información tributaria del lugar de negocios |

## Navigation properties (54)

Use `GET /b1s/v2/BusinessPlaces(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `UserDefaultGroups` | Collection([UserDefaultGroup](../Entidades/UserDefaultGroups.md)) | [UserDefaultGroups](UserDefaultGroups.md) |  | Grupos de valores predeterminados de usuario |
| `StockTransfers` | Collection([StockTransfer](../Entidades/StockTransfers.md)) | [StockTransfers](StockTransfers.md) |  | Transferencias de stock |
| `PurchaseQuotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseQuotations](PurchaseQuotations.md) |  | Ofertas de compra |
| `VendorPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [VendorPayments](VendorPayments.md) |  | Pagos efectuados |
| `CorrectionInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoiceReversal](CorrectionInvoiceReversal.md) |  | Anulación de factura de corrección de clientes |
| `CorrectionInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoice](CorrectionInvoice.md) |  | Factura de corrección de clientes |
| `PurchaseDeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDeliveryNotes](PurchaseDeliveryNotes.md) |  | Pedidos de entrada de mercancías |
| `CorrectionPurchaseInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoice](CorrectionPurchaseInvoice.md) |  | Factura de corrección de proveedores |
| `InventoryCountingDrafts` | Collection([InventoryCountingDraft](../Entidades/InventoryCountingDrafts.md)) | [InventoryCountingDrafts](InventoryCountingDrafts.md) |  | Borradores de recuento de inventario |
| `InventoryGenEntries` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenEntries](InventoryGenEntries.md) |  | Entradas de mercancías |
| `AssetRetirement` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetRetirement](AssetRetirement.md) |  | Baja de activos |
| `AssetTransfer` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetTransfer](AssetTransfer.md) |  | Transferencia de activos |
| `AssetRevaluations` | Collection([AssetRevaluation](../Entidades/AssetRevaluations.md)) | [AssetRevaluations](AssetRevaluations.md) |  | Revalorizaciones de activos |
| `EmployeesInfo` | Collection([EmployeeInfo](../Entidades/EmployeesInfo.md)) | [EmployeesInfo](EmployeesInfo.md) |  | Empleados |
| `AssetManualDepreciation` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetManualDepreciation](AssetManualDepreciation.md) |  | Amortización manual de activos |
| `AssetClasses` | Collection([AssetClass](../Entidades/AssetClasses.md)) | [AssetClasses](AssetClasses.md) |  | Clases de activos |
| `Orders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Orders](Orders.md) |  | Pedidos de cliente (órdenes de venta) |
| `AssetCapitalization` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetCapitalization](AssetCapitalization.md) |  | Capitalización de activos fijos |
| `InventoryGenExits` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenExits](InventoryGenExits.md) |  | Salidas de mercancías |
| `Drafts` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Drafts](Drafts.md) |  | Borradores de documentos |
| `InventoryTransferRequests` | Collection([StockTransfer](../Entidades/StockTransfers.md)) | [InventoryTransferRequests](InventoryTransferRequests.md) |  | Solicitudes de transferencia de stock |
| `InventoryCountings` | Collection([InventoryCounting](../Entidades/InventoryCountings.md)) | [InventoryCountings](InventoryCountings.md) |  | Recuentos de inventario |
| `InventoryOpeningBalances` | Collection([InventoryOpeningBalance](../Entidades/InventoryOpeningBalances.md)) | [InventoryOpeningBalances](InventoryOpeningBalances.md) |  | Saldos iniciales de inventario |
| `InventoryPostings` | Collection([InventoryPosting](../Entidades/InventoryPostings.md)) | [InventoryPostings](InventoryPostings.md) |  | Contabilizaciones de inventario |
| `ReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [ReturnRequest](ReturnRequest.md) |  | Solicitudes de devolución de clientes |
| `DeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DeliveryNotes](DeliveryNotes.md) |  | Entregas |
| `PurchaseInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseInvoices](PurchaseInvoices.md) |  | Facturas de proveedores |
| `StockTransferDrafts` | Collection([StockTransfer](../Entidades/StockTransfers.md)) | [StockTransferDrafts](StockTransferDrafts.md) |  | Borradores de transferencias de stock |
| `SelfInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfInvoices](SelfInvoices.md) |  | Autofacturas |
| `Invoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Invoices](Invoices.md) |  | Facturas de clientes |
| `CreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CreditNotes](CreditNotes.md) |  | Notas de crédito de clientes |
| `AssetCapitalizationCreditMemo` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetCapitalizationCreditMemo](AssetCapitalizationCreditMemo.md) |  | Nota de crédito de capitalización de activos |
| `PaymentDrafts` | Collection([Payment](../Entidades/VendorPayments.md)) | [PaymentDrafts](PaymentDrafts.md) |  | Borradores de pagos |
| `PurchaseCreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseCreditNotes](PurchaseCreditNotes.md) |  | Notas de crédito de proveedores |
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
| `Deposits` | Collection([Deposit](../Entidades/Deposits.md)) | [Deposits](Deposits.md) |  | Depósitos |
| `PurchaseRequests` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseRequests](PurchaseRequests.md) |  | Solicitudes de compra |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | DefaultCustomerID → CardCode | Socio de negocios |
| `Warehouse` | [Warehouse](../Entidades/Warehouses.md) | [Warehouses](Warehouses.md) | DefaultWarehouseID → WarehouseCode | Almacén |
| `BPFiscalRegistryID` | [BPFiscalRegistryID](../Entidades/BPFiscalRegistryID.md) | [BPFiscalRegistryID](BPFiscalRegistryID.md) | DefaultTaxCode → Numerator | ID de registro fiscal del socio de negocios |
| `BrazilNumericIndexer` | [BrazilNumericIndexer](../Entidades/BrazilNumericIndexers.md) | [BrazilNumericIndexers](BrazilNumericIndexers.md) | NatureOfCompanyCode → ID | Brasil - Indexadores numéricos |
| `BrazilStringIndexer` | [BrazilStringIndexer](../Entidades/BrazilStringIndexers.md) | [BrazilStringIndexers](BrazilStringIndexers.md) | CreditContributionOriginCode → ID | Brasil - Indexadores de cadenas |
| `County2` | [County](../Entidades/Counties.md) | [Counties](Counties.md) | County → AbsId | Condados |
| `Country2` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | Country → Code | Países/Regiones |
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | PaymentClearingAccount → Code | Plan de cuentas (cuentas de mayor) |
