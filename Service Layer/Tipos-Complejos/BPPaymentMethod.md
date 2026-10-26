# BPPaymentMethod — Vías de pago del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BPPaymentMethod`
- **Descripción (ES):** Vías de pago del socio de negocios
- **Description (EN):** Business Partner Payment Method
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PaymentMethodCode` | Edm.String | Yes | Payment Method Code | Código de vía de pago |
| 2 | `RowNumber` | Edm.Int32 | Yes | Row Number | Número de línea |
| 3 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |

## Used by (properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`BPPaymentMethods`
