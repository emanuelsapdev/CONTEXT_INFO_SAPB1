# SalesTaxInvoices — Facturas de impuestos de venta

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SalesTaxInvoices`
- **Descripción (ES):** Facturas de impuestos de venta
- **Entity type:** `SalesTaxInvoice` (open type: accepts dynamic/UDF properties)
- **Key:** `DocEntry` (Edm.Int32)
- **DB tables (main / lines):** [OTSI](../../Tablas%20SAP%20B1/OTSI.md), [TSI1](../../Tablas%20SAP%20B1/TSI1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 31 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SalesTaxInvoices?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SalesTaxInvoices/$count` | Contar |
| Get by key | `GET /b1s/v2/SalesTaxInvoices(1)` | Obtener por clave |
| Create | `POST /b1s/v2/SalesTaxInvoices` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SalesTaxInvoices(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SalesTaxInvoices(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/SalesTaxInvoices(1)` (only if the B1 object allows removal) | Borrar |

## Properties (31)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` 🔑 | Edm.Int32 | No | Document Entry | DocEntry (clave interna del documento) |
| 2 | `DocNum` | Edm.Int32 | Yes | Document Number | Número de documento |
| 3 | `DocType` | [BoTaxInvoiceTypes](../Enums/BoTaxInvoiceTypes.md) | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 4 | `Printed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Printed | Impreso |
| 5 | `DocDate` | Edm.DateTimeOffset | Yes | Document Date | Fecha de contabilización del documento |
| 6 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 7 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 8 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 9 | `DocDueDate` | Edm.DateTimeOffset | Yes | Document Due Date | Fecha de vencimiento del documento |
| 10 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 11 | `Segment` | Edm.Int32 | Yes | Segment | Segmento |
| 12 | `ContactPersonCode` | Edm.Int32 | Yes | Contact Person Code | Código de persona de contacto |
| 13 | `TaxDate` | Edm.DateTimeOffset | Yes | Tax Date | Fecha del documento (fecha de impuestos) |
| 14 | `Comments` | Edm.String | Yes | Comments | Comentarios |
| 15 | `ShipToCode` | Edm.String | Yes | Ship To Code | Código de dirección de envío |
| 16 | `Address` | Edm.String | Yes | Address | Dirección |
| 17 | `Address2` | Edm.String | Yes | Address 2 | Dirección 2 |
| 18 | `CurrencySource` | [BoCurrencySources](../Enums/BoCurrencySources.md) | Yes | Currency Source | Origen de la moneda |
| 19 | `DocCurrency` | Edm.String | Yes | Document Currency | Moneda del documento |
| 20 | `CustomerOrVendorRefNo` | Edm.String | Yes | Customer Or Vendor Ref Number | N.º de referencia del cliente o proveedor |
| 21 | `CustomerOrVendorName` | Edm.String | Yes | Customer Or Vendor Name | Nombre del cliente o proveedor |
| 22 | `CancelDate` | Edm.DateTimeOffset | Yes | Cancel Date | Fecha de cancelación |
| 23 | `DocumentTotal` | Edm.Double | Yes | Document Total | Total del documento |
| 24 | `TaxTotal` | Edm.Double | Yes | Tax Total | Total de impuestos |
| 25 | `PaymentRefNo` | Edm.String | Yes | Payment Ref Number | N.º de referencia del pago |
| 26 | `PaymentRefDate` | Edm.DateTimeOffset | Yes | Payment Ref Date | Fecha de referencia del pago |
| 27 | `AlterationRevision` | Edm.Int32 | Yes | Alteration Revision | Revisión de modificación |
| 28 | `SalesTaxInvoiceLines` | Collection([SalesTaxInvoiceLine](../Tipos-Complejos/SalesTaxInvoiceLine.md)) | Yes | Sales Tax Invoice Lines | Líneas de la factura de impuestos de venta |
| 29 | `SalesTaxInvoiceOperationCodes` | Collection([SalesTaxInvoiceOperationCode](../Tipos-Complejos/SalesTaxInvoiceOperationCode.md)) | Yes | Sales Tax Invoice Operation Codes | Códigos de operación de la factura de impuestos de venta |
| 30 | `SalesTaxInvoiceDocumentReferences` | Collection([SalesTaxInvoiceDocumentReference](../Tipos-Complejos/SalesTaxInvoiceDocumentReference.md)) | Yes | Sales Tax Invoice Document References | Referencias de documentos de la factura de impuestos de venta |
| 31 | `SalesTaxInvoiceLinkedDownPayments` | Collection([SalesTaxInvoiceLinkedDownPayment](../Tipos-Complejos/SalesTaxInvoiceLinkedDownPayment.md)) | Yes | Sales Tax Invoice Linked Down Payments | Anticipos vinculados de la factura de impuestos de venta |

## Navigation properties (1)

Use `GET /b1s/v2/SalesTaxInvoices(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CardCode → CardCode | Socio de negocios |
