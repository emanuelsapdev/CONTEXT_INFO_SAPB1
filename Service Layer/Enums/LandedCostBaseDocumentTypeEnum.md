# LandedCostBaseDocumentTypeEnum — Tipo de documento base del costo de importación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `LandedCostBaseDocumentTypeEnum`
- **Descripción (ES):** Tipo de documento base del costo de importación
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `asDefault` | 0 | Default | Predeterminado |
| `asEmpty` | 1 | Empty | Vacío |
| `asGoodsReceiptPO` | 2 | Goods Receipt PO | Pedido de entrada de mercancías |
| `asLandedCosts` | 3 | Landed Costs | Costos de importación |
| `asPurchaseInvoice` | 4 | Purchase Invoice | Factura de proveedores |

## Used by (1 properties)

- [LandedCost_ItemLine](../Tipos-Complejos/LandedCost_ItemLine.md).`BaseDocumentType`
