# IdentificationCodeTypeEnum — Tipo de código de identificación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `IdentificationCodeTypeEnum`
- **Descripción (ES):** Tipo de código de identificación
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `idctOrder` | 0 | Order | Pedido |
| `idctDelivery` | 1 | Delivery | Entrega |
| `idctInvoice` | 2 | Invoice | Factura |
| `idctCreditNote` | 3 | Credit Note | Nota de crédito |
| `idctStandardItemTypeIdentification` | 4 | Standard Item Type Identification | Identificación estándar del tipo de artículo |
| `idctItemCommodityClassification` | 5 | Item Commodity Classification | Clasificación de mercancía del artículo |

## Used by (1 properties)

- [IdentificationCode](../Entidades/IdentificationCodes.md).`Codelist`
