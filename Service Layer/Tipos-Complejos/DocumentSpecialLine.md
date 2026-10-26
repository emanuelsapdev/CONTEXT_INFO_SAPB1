# DocumentSpecialLine — Líneas especiales del documento (texto/subtotal)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocumentSpecialLine`
- **Descripción (ES):** Líneas especiales del documento (texto/subtotal)
- **Description (EN):** Document Special Line

- **Properties:** 23

## Properties (23)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `AfterLineNumber` | Edm.Int32 | Yes | After Line Number | Después del número de línea |
| 3 | `OrderNumber` | Edm.Int32 | Yes | Order Number | Número de pedido |
| 4 | `LineType` | [BoDocSpecialLineType](../Enums/BoDocSpecialLineType.md) | Yes | Line Type | Tipo de línea |
| 5 | `Subtotal` | Edm.Double | Yes | Subtotal | Subtotal |
| 6 | `LineText` | Edm.String | Yes | Line Text | Texto de línea |
| 7 | `SubtotalFC` | Edm.Double | Yes | Subtotal FC (foreign currency) | Subtotal (ME) |
| 8 | `SubtotalSC` | Edm.Double | Yes | Subtotal SC (system currency) | Subtotal (moneda del sistema) |
| 9 | `TaxAmount` | Edm.Double | Yes | Tax Amount | Importe de impuestos |
| 10 | `TaxAmountFC` | Edm.Double | Yes | Tax Amount FC (foreign currency) | Importe de impuestos (ME) |
| 11 | `TaxAmountSC` | Edm.Double | Yes | Tax Amount SC (system currency) | Importe de impuestos (moneda del sistema) |
| 12 | `Freight1` | Edm.Double | Yes | Freight 1 | Flete 1 |
| 13 | `Freight1FC` | Edm.Double | Yes | Freight 1 FC (foreign currency) | Flete 1 (ME) |
| 14 | `Freight1SC` | Edm.Double | Yes | Freight 1 SC (system currency) | Flete 1 (moneda del sistema) |
| 15 | `Freight2` | Edm.Double | Yes | Freight 2 | Flete 2 |
| 16 | `Freight2FC` | Edm.Double | Yes | Freight 2 FC (foreign currency) | Flete 2 (ME) |
| 17 | `Freight2SC` | Edm.Double | Yes | Freight 2 SC (system currency) | Flete 2 (moneda del sistema) |
| 18 | `Freight3` | Edm.Double | Yes | Freight 3 | Flete 3 |
| 19 | `Freight3FC` | Edm.Double | Yes | Freight 3 FC (foreign currency) | Flete 3 (ME) |
| 20 | `Freight3SC` | Edm.Double | Yes | Freight 3 SC (system currency) | Flete 3 (moneda del sistema) |
| 21 | `GrossTotal` | Edm.Double | Yes | Gross Total | Total bruto |
| 22 | `GrossTotalFC` | Edm.Double | Yes | Gross Total FC (foreign currency) | Total bruto (ME) |
| 23 | `GrossTotalSC` | Edm.Double | Yes | Gross Total SC (system currency) | Total bruto (moneda del sistema) |

## Used by (properties)

- [Document](../Entidades/PurchaseQuotations.md).`DocumentSpecialLines`
