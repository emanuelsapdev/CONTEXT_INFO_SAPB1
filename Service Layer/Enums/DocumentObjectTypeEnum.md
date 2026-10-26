# DocumentObjectTypeEnum — Tipo de objeto del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `DocumentObjectTypeEnum`
- **Descripción (ES):** Tipo de objeto del documento
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `dc_ArInvoice` | 13 | Ar Invoice | Factura de clientes |
| `dc_Delivery` | 15 | Delivery | Entrega |
| `dc_GoodsReturn` | 21 | Goods Return | Devolución de mercancías |
| `dc_InventoryTransfer` | 67 | Inventory Transfer | Transferencia de stock |

## Used by (2 properties)

- [RecurringTransactionTemplate](../Entidades/RecurringTransactionTemplates.md).`DocumentObjectType`
- [TransportationDocumentLineData](../Tipos-Complejos/TransportationDocumentLineData.md).`DocType`
