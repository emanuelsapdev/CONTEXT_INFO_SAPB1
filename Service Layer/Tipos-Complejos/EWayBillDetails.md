# EWayBillDetails — Detalles de E-Way Bill

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EWayBillDetails`
- **Descripción (ES):** Detalles de E-Way Bill
- **Description (EN):** E Way Bill Details

- **Properties:** 35

## Properties (35)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `SupplyType` | [EWBSupplyTypeEnum](../Enums/EWBSupplyTypeEnum.md) | Yes | Supply Type | Tipo de suministro |
| 3 | `SubType` | Edm.Int32 | Yes | Sub Type | Subtipo |
| 4 | `DocumentType` | Edm.String | Yes | Document Type | Tipo de documento |
| 5 | `TransportationMode` | Edm.Int32 | Yes | Transportation Mode | Modo de transporte |
| 6 | `Distance` | Edm.Double | Yes | Distance | Distancia |
| 7 | `TransporterDocNo` | Edm.String | Yes | Transporter Document Number | N.º de documento del transportista |
| 8 | `TransporterDocDate` | Edm.DateTimeOffset | Yes | Transporter Document Date | Fecha del documento del transportista |
| 9 | `VehicleType` | Edm.String | Yes | Vehicle Type | Tipo de vehículo |
| 10 | `VehicleNo` | Edm.String | Yes | Vehicle Number | Número de vehículo |
| 11 | `EWayBillNo` | Edm.String | Yes | E Way Bill Number | Número de E-Way Bill |
| 12 | `EWayBillDate` | Edm.DateTimeOffset | Yes | E Way Bill Date | Fecha de E-Way Bill |
| 13 | `BillFromName` | Edm.String | Yes | Bill From Name | Nombre de facturación desde |
| 14 | `BillFromGSTIN` | Edm.String | Yes | Bill From GSTIN | GSTIN de facturación desde |
| 15 | `BillFromStateGSTCode` | Edm.String | Yes | Bill From State GST Code | Código GST del estado de facturación desde |
| 16 | `DispatchFromAddress1` | Edm.String | Yes | Dispatch From Address 1 | Dirección de despacho 1 |
| 17 | `DispatchFromAddress2` | Edm.String | Yes | Dispatch From Address 2 | Dirección de despacho 2 |
| 18 | `DispatchFromZipCode` | Edm.String | Yes | Dispatch From Zip Code | Código postal de despacho |
| 19 | `DispatchFromStateGSTCode` | Edm.String | Yes | Dispatch From State GST Code | Código GST del estado de despacho |
| 20 | `BillToName` | Edm.String | Yes | Bill To Name | Nombre de facturación |
| 21 | `BillToGSTIN` | Edm.String | Yes | Bill To GSTIN | GSTIN de facturación |
| 22 | `BillToStateGSTCode` | Edm.String | Yes | Bill To State GST Code | Código GST del estado de facturación |
| 23 | `ShipToAddress1` | Edm.String | Yes | Ship To Address 1 | Dirección de envío 1 |
| 24 | `ShipToAddress2` | Edm.String | Yes | Ship To Address 2 | Dirección de envío 2 |
| 25 | `ShipToZipCode` | Edm.String | Yes | Ship To Zip Code | Código postal de envío |
| 26 | `ShipToStateGSTCode` | Edm.String | Yes | Ship To State GST Code | Código GST del estado de envío |
| 27 | `MainHSNEntry` | Edm.Int32 | Yes | Main HSN Entry | Entrada HSN principal |
| 28 | `DispatchFromPlace` | Edm.String | Yes | Dispatch From Place | Lugar de despacho |
| 29 | `ShipToPlace` | Edm.String | Yes | Ship To Place | Lugar de envío |
| 30 | `TransporterID` | Edm.String | Yes | Transporter ID | ID del transportista |
| 31 | `TransporterName` | Edm.String | Yes | Transporter Name | Nombre del transportista |
| 32 | `EWayBillExpirationDate` | Edm.DateTimeOffset | Yes | E Way Bill Expiration Date | Fecha de vencimiento de E-Way Bill |
| 33 | `TransporterEntry` | Edm.Int32 | Yes | Transporter Entry | Entrada del transportista |
| 34 | `TransporterLineNumber` | Edm.Int32 | Yes | Transporter Line Number | Línea del transportista |
| 35 | `TransactionType` | [EWBTransactionTypeEnum](../Enums/EWBTransactionTypeEnum.md) | Yes | Transaction Type | Tipo de transacción |

## Used by (properties)

- [Document](../Entidades/PurchaseQuotations.md).`EWayBillDetails`
