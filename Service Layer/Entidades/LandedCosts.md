# LandedCosts — Costos de importación (landed costs)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `LandedCosts`
- **Descripción (ES):** Costos de importación (landed costs)
- **Entity type:** `LandedCost` (open type: accepts dynamic/UDF properties)
- **Key:** `DocEntry` (Edm.Int32)
- **DB tables (main / lines):** [OIPF](../../Tablas%20SAP%20B1/OIPF.md), [IPF1](../../Tablas%20SAP%20B1/IPF1.md), [IPF2](../../Tablas%20SAP%20B1/IPF2.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 39 · **Navigation properties:** 4 · **Bound actions:** 2

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/LandedCosts?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/LandedCosts/$count` | Contar |
| Get by key | `GET /b1s/v2/LandedCosts(1)` | Obtener por clave |
| Create | `POST /b1s/v2/LandedCosts` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/LandedCosts(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/LandedCosts(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/LandedCosts(1)` (only if the B1 object allows removal) | Borrar |
| Action `CloseLandedCost` | `POST /b1s/v2/LandedCosts(1)/CloseLandedCost` | Cerrar costo de importación |
| Action `CancelLandedCost` | `POST /b1s/v2/LandedCosts(1)/CancelLandedCost` | Cancelar costo de importación |

## Properties (39)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` 🔑 | Edm.Int32 | No | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LandedCostNumber` | Edm.Int32 | Yes | Landed Cost Number | Número de costo de importación |
| 3 | `PostingDate` | Edm.DateTimeOffset | Yes | Posting Date | Fecha de contabilización |
| 4 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 5 | `VendorCode` | Edm.String | Yes | Vendor Code | Código de proveedor |
| 6 | `VendorName` | Edm.String | Yes | Vendor Name | Nombre del proveedor |
| 7 | `Broker` | Edm.String | Yes | Broker | Agente |
| 8 | `BrokerName` | Edm.String | Yes | Broker Name | Nombre del agente |
| 9 | `ClosedDocument` | [LandedCostDocStatusEnum](../Enums/LandedCostDocStatusEnum.md) | Yes | Closed Document | Documento cerrado |
| 10 | `FileNumber` | Edm.String | Yes | File Number | Número de archivo |
| 11 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 12 | `Reference` | Edm.String | Yes | Reference | Referencia |
| 13 | `DocumentCurrency` | Edm.String | Yes | Document Currency | Moneda del documento |
| 14 | `DocumentRate` | Edm.Double | Yes | Document Rate | Tipo de cambio del documento |
| 15 | `ProjectedCustoms` | Edm.Double | Yes | Projected Customs | Aduana proyectada |
| 16 | `ActualCustoms` | Edm.Double | Yes | Actual Customs | Aduana real |
| 17 | `ActualCustomsFC` | Edm.Double | Yes | Actual Customs FC (foreign currency) | Aduana real (ME) |
| 18 | `Tax1` | Edm.Double | Yes | Tax 1 | Impuesto 1 |
| 19 | `Tax2` | Edm.Double | Yes | Tax 2 | Impuesto 2 |
| 20 | `BeforeTax` | Edm.Double | Yes | Before Tax | Antes de impuestos |
| 21 | `Total` | Edm.Double | Yes | Total | Total |
| 22 | `TotalFreightCharges` | Edm.Double | Yes | Total Freight Charges | Total de gastos adicionales |
| 23 | `ProjectedCustomsFC` | Edm.Double | Yes | Projected Customs FC (foreign currency) | Aduana proyectada (ME) |
| 24 | `Tax1FC` | Edm.Double | Yes | Tax 1 FC (foreign currency) | Impuesto 1 (ME) |
| 25 | `Tax2FC` | Edm.Double | Yes | Tax 2 FC (foreign currency) | Impuesto 2 (ME) |
| 26 | `BeforeTaxFC` | Edm.Double | Yes | Before Tax FC (foreign currency) | Antes de impuestos (ME) |
| 27 | `TotalFC` | Edm.Double | Yes | Total FC (foreign currency) | Total (ME) |
| 28 | `TotalFreightChargesFC` | Edm.Double | Yes | Total Freight Charges FC (foreign currency) | Total de gastos adicionales (ME) |
| 29 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 30 | `CustomsAffectsInventory` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Customs Affects Inventory | Aduana afecta el inventario |
| 31 | `AmountToBalance` | Edm.Double | Yes | Amount To Balance | Importe a saldar |
| 32 | `AmountToBalanceFC` | Edm.Double | Yes | Amount To Balance FC (foreign currency) | Importe a saldar (ME) |
| 33 | `BillofLadingNumber` | Edm.String | Yes | Billof Lading Number | Número de conocimiento de embarque |
| 34 | `TransportType` | Edm.Int32 | Yes | Transport Type | Tipo de transporte |
| 35 | `TransactionNumber` | Edm.Int32 | Yes | Transaction Number | Número de transacción |
| 36 | `JournalRemarks` | Edm.String | Yes | Journal Remarks | Comentarios del asiento |
| 37 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 38 | `LandedCost_ItemLines` | Collection([LandedCost_ItemLine](../Tipos-Complejos/LandedCost_ItemLine.md)) | Yes | Landed Cost Item Lines | Líneas de artículos del costo de importación |
| 39 | `LandedCost_CostLines` | Collection([LandedCost_CostLine](../Tipos-Complejos/LandedCost_CostLine.md)) | Yes | Landed Cost Cost Lines | Líneas de costos del costo de importación |

## Navigation properties (4)

Use `GET /b1s/v2/LandedCosts(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | VendorCode → CardCode | Socio de negocios |
| `ShippingType` | [ShippingType](../Entidades/ShippingTypes.md) | [ShippingTypes](ShippingTypes.md) | TransportType → Code | Clase de expedición |
| `JournalEntry` | [JournalEntry](../Entidades/JournalEntries.md) | [JournalEntries](JournalEntries.md) | TransactionNumber → JdtNum | Asientos contables |
| `PurchaseDeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDeliveryNotes](PurchaseDeliveryNotes.md) |  | Pedidos de entrada de mercancías |

## Bound actions (2)

### CloseLandedCost

- **Descripción (ES):** Cerrar costo de importación
- **Request:** `POST /b1s/v2/LandedCosts(1)/CloseLandedCost`

### CancelLandedCost

- **Descripción (ES):** Cancelar costo de importación
- **Request:** `POST /b1s/v2/LandedCosts(1)/CancelLandedCost`

