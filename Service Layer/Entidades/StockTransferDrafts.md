# StockTransferDrafts — Borradores de transferencias de stock

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `StockTransferDrafts`
- **Descripción (ES):** Borradores de transferencias de stock
- **Entity type:** `StockTransfer` (open type: accepts dynamic/UDF properties)
- **Key:** `DocEntry` (Edm.Int32)
- **DB tables (main / lines):** [ODRF](../../Tablas%20SAP%20B1/ODRF.md), [DRF1](../../Tablas%20SAP%20B1/DRF1.md)
- **ETag / optimistic concurrency:** No
- **Other entity sets with the same type:** [StockTransfers](StockTransfers.md), [InventoryTransferRequests](InventoryTransferRequests.md)
- **Properties:** 60 · **Navigation properties:** 7 · **Bound actions:** 3

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/StockTransferDrafts?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/StockTransferDrafts/$count` | Contar |
| Get by key | `GET /b1s/v2/StockTransferDrafts(1)` | Obtener por clave |
| Create | `POST /b1s/v2/StockTransferDrafts` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/StockTransferDrafts(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/StockTransferDrafts(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/StockTransferDrafts(1)` (only if the B1 object allows removal) | Borrar |
| Action `Cancel` | `POST /b1s/v2/StockTransferDrafts(1)/Cancel` | Cancelar |
| Action `Close` | `POST /b1s/v2/StockTransferDrafts(1)/Close` | Cerrar |
| Action `SaveDraftToDocument` | `POST /b1s/v2/StockTransferDrafts(1)/SaveDraftToDocument` | Guardar borrador como documento |

## Properties (60)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` 🔑 | Edm.Int32 | No | Document Entry | DocEntry (clave interna del documento) |
| 2 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 3 | `Printed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Printed | Impreso |
| 4 | `DocDate` | Edm.DateTimeOffset | Yes | Document Date | Fecha de contabilización del documento |
| 5 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 6 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 7 | `CardName` | Edm.String | Yes | Card Name | Nombre del socio de negocios |
| 8 | `Address` | Edm.String | Yes | Address | Dirección |
| 9 | `Reference1` | Edm.String | Yes | Reference 1 | Referencia 1 |
| 10 | `Reference2` | Edm.String | Yes | Reference 2 | Referencia 2 |
| 11 | `Comments` | Edm.String | Yes | Comments | Comentarios |
| 12 | `JournalMemo` | Edm.String | Yes | Journal Memo | Comentario del asiento |
| 13 | `PriceList` | Edm.Int32 | Yes | Price List | Lista de precios |
| 14 | `SalesPersonCode` | Edm.Int32 | Yes | Sales Person Code | Código del empleado de ventas |
| 15 | `FromWarehouse` | Edm.String | Yes | From Warehouse | Almacén de origen |
| 16 | `ToWarehouse` | Edm.String | Yes | To Warehouse | Almacén de destino |
| 17 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 18 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 19 | `FinancialPeriod` | Edm.Int32 | Yes | Financial Period | Período contable |
| 20 | `TransNum` | Edm.Int32 | Yes | Trans Number | Número de transacción |
| 21 | `DocNum` | Edm.Int32 | Yes | Document Number | Número de documento |
| 22 | `TaxDate` | Edm.DateTimeOffset | Yes | Tax Date | Fecha del documento (fecha de impuestos) |
| 23 | `ContactPerson` | Edm.Int32 | Yes | Contact Person | Persona de contacto |
| 24 | `FolioPrefixString` | Edm.String | Yes | Folio Prefix String | Prefijo de folio (letra) |
| 25 | `FolioNumber` | Edm.Int32 | Yes | Folio Number | Número de folio |
| 26 | `DocObjectCode` | Edm.String | Yes | Document Object Code | Código de objeto del documento |
| 27 | `AuthorizationStatus` | [StockTransferAuthorizationStatusEnum](../Enums/StockTransferAuthorizationStatusEnum.md) | Yes | Authorization Status | Estado de autorización |
| 28 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |
| 29 | `BPLName` | Edm.String | Yes | Branch Name | Nombre de la sucursal |
| 30 | `VATRegNum` | Edm.String | Yes | VAT Reg Number | Número de registro de IVA |
| 31 | `AuthorizationCode` | Edm.String | Yes | Authorization Code | Código de autorización |
| 32 | `StartDeliveryDate` | Edm.DateTimeOffset | Yes | Start Delivery Date | Fecha de inicio de entrega |
| 33 | `StartDeliveryTime` | Edm.TimeOfDay | Yes | Start Delivery Time | Hora de inicio de entrega |
| 34 | `EndDeliveryDate` | Edm.DateTimeOffset | Yes | End Delivery Date | Fecha de fin de entrega |
| 35 | `EndDeliveryTime` | Edm.TimeOfDay | Yes | End Delivery Time | Hora de fin de entrega |
| 36 | `VehiclePlate` | Edm.String | Yes | Vehicle Plate | Patente del vehículo |
| 37 | `ATDocumentType` | Edm.String | Yes | AT Document Type | Tipo de documento AT |
| 38 | `EDocExportFormat` | Edm.Int32 | Yes | E Document Export Format | Formato de exportación del documento electrónico |
| 39 | `ElecCommStatus` | [ElecCommStatusEnum](../Enums/ElecCommStatusEnum.md) | Yes | Elec Comm Status | Estado de comunicación electrónica |
| 40 | `ElecCommMessage` | Edm.String | Yes | Elec Comm Message | Mensaje de comunicación electrónica |
| 41 | `PointOfIssueCode` | Edm.String | Yes | Point Of Issue Code | Código de punto de emisión |
| 42 | `Letter` | [FolioLetterEnum](../Enums/FolioLetterEnum.md) | Yes | Letter | Carta |
| 43 | `FolioNumberFrom` | Edm.Int32 | Yes | Folio Number From | Número de folio desde |
| 44 | `FolioNumberTo` | Edm.Int32 | Yes | Folio Number To | Número de folio hasta |
| 45 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 46 | `DocumentStatus` | [BoStatus](../Enums/BoStatus.md) | Yes | Document Status | Estado del documento |
| 47 | `ShipToCode` | Edm.String | Yes | Ship To Code | Código de dirección de envío |
| 48 | `SAPPassport` | Edm.String | Yes | SAP Passport | SAP Passport |
| 49 | `LastPageFolioNumber` | Edm.Int32 | Yes | Last Page Folio Number | Número de folio de la última página |
| 50 | `DutyStatus` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Duty Status | Estado de aranceles |
| 51 | `CreateQRCodeFrom` | Edm.String | Yes | Create QR Code From | Crear código QR desde |
| 52 | `U_B1SYS_CAI` | Edm.String | Yes | [AR localization] CAI | [Loc. AR] CAI (Código de Autorización de Impresión) |
| 53 | `U_B1SYS_CAI_DATE` | Edm.DateTimeOffset | Yes | [AR localization] CAI DATE | [Loc. AR] Fecha de vencimiento del CAI |
| 54 | `U_B1SYS_ECM2_LINK` | Edm.Int32 | Yes | [AR localization] ECM 2 LINK | [Loc. AR] Vínculo a comunicación electrónica (ECM) |
| 55 | `StockTransfer_ApprovalRequests` | Collection([StockTransfer_ApprovalRequest](../Tipos-Complejos/StockTransfer_ApprovalRequest.md)) | Yes | Stock Transfer Approval Requests | Solicitudes de autorización de la transferencia de stock |
| 56 | `ElectronicProtocols` | Collection([ElectronicProtocol](../Tipos-Complejos/ElectronicProtocol.md)) | Yes | Electronic Protocols | Protocolos electrónicos |
| 57 | `StockTransferLines` | Collection([StockTransferLine](../Tipos-Complejos/StockTransferLine.md)) | Yes | Stock Transfer Lines | Líneas de la transferencia de stock |
| 58 | `StockTransferTaxExtension` | [StockTransferTaxExtension](../Tipos-Complejos/StockTransferTaxExtension.md) | Yes | Stock Transfer Tax Extension | Extensión de impuestos de la transferencia de stock |
| 59 | `DocumentReferences` | Collection([DocumentReference](../Tipos-Complejos/DocumentReference.md)) | Yes | Document References | Referencias del documento |
| 60 | `EDeliveryInfo` | [EDeliveryInfo](../Tipos-Complejos/EDeliveryInfo.md) | Yes | E Delivery Information | Información de entrega electrónica |

## Navigation properties (7)

Use `GET /b1s/v2/StockTransferDrafts(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CardCode → CardCode | Socio de negocios |
| `PriceList2` | [PriceList](../Entidades/PriceLists.md) | — | PriceList → PriceListNo | Listas de precios |
| `SalesPerson` | [SalesPerson](../Entidades/SalesPersons.md) | [SalesPersons](SalesPersons.md) | SalesPersonCode → SalesEmployeeCode | Empleado de ventas |
| `Warehouse` | [Warehouse](../Entidades/Warehouses.md) | [Warehouses](Warehouses.md) | FromWarehouse → WarehouseCode | Almacén |
| `JournalEntry` | [JournalEntry](../Entidades/JournalEntries.md) | [JournalEntries](JournalEntries.md) | TransNum → JdtNum | Asientos contables |
| `BusinessPlace` | [BusinessPlace](../Entidades/BusinessPlaces.md) | [BusinessPlaces](BusinessPlaces.md) | BPLID → BPLID | Lugar de negocios |
| `PaymentTermsType` | [PaymentTermsType](../Entidades/PaymentTermsTypes.md) | [PaymentTermsTypes](PaymentTermsTypes.md) | PriceList → GroupNumber | Condiciones de pago |

## Bound actions (3)

### Cancel

- **Descripción (ES):** Cancelar
- **Request:** `POST /b1s/v2/StockTransferDrafts(1)/Cancel`

### Close

- **Descripción (ES):** Cerrar
- **Request:** `POST /b1s/v2/StockTransferDrafts(1)/Close`

### SaveDraftToDocument

- **Descripción (ES):** Guardar borrador como documento
- **Request:** `POST /b1s/v2/StockTransferDrafts(1)/SaveDraftToDocument`


## Service operations that use this type

- [`InventoryTransferRequestsService_GetApprovalTemplates`](../Servicios/InventoryTransferRequestsService.md#inventorytransferrequestsservice_getapprovaltemplates)
- [`StockTransferDraftService_GetApprovalTemplates`](../Servicios/StockTransferDraftService.md#stocktransferdraftservice_getapprovaltemplates)
- [`StockTransferService_GetApprovalTemplates`](../Servicios/StockTransferService.md#stocktransferservice_getapprovaltemplates)
