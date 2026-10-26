# DocumentPriceSourceEnum — Origen del precio en el documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `DocumentPriceSourceEnum`
- **Descripción (ES):** Origen del precio en el documento
- **Underlying type:** Edm.Int32
- **Members:** 17

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `dpsSpecialPricesForBusinessPartner` | 0 | Special Prices For Business Partner | Precios especiales del socio de negocios |
| `dpsManual` | 1 | Manual | Manual |
| `dpsActivePriceListDiscountGroups` | 2 | Active Price List Discount Groups | Lista de precios activa + grupos de descuento |
| `dpsActivePriceList` | 3 | Active Price List | Lista de precios activa |
| `dpsInactivePriceList` | 4 | Inactive Price List | Lista de precios inactiva |
| `dpsBlanketAgreement` | 5 | Blanket Agreement | Acuerdo global |
| `dpsPeriodAndVolumeDiscounts` | 6 | Period And Volume Discounts | Descuentos por período y volumen |
| `dpsPeriodAndVolumeDiscountsDiscountGroups` | 7 | Period And Volume Discounts Discount Groups | Descuentos por período y volumen + grupos de descuento |
| `dpsInactivePriceListDiscountGroups` | 8 | Inactive Price List Discount Groups | Lista de precios inactiva + grupos de descuento |
| `dpsNewSpecialPricesForBusinessPartner` | 9 | New Special Prices For Business Partner | Nuevo: precios especiales del socio de negocios |
| `dpsNewActivePriceListDiscountGroups` | 10 | New Active Price List Discount Groups | Nuevo: lista activa + grupos de descuento |
| `dpsNewActivePriceList` | 11 | New Active Price List | Nuevo: lista de precios activa |
| `dpsNewInactivePriceList` | 12 | New Inactive Price List | Nuevo: lista de precios inactiva |
| `dpsNewBlanketAgreement` | 13 | New Blanket Agreement | Nuevo: acuerdo global |
| `dpsNewPeriodAndVolumeDiscounts` | 14 | New Period And Volume Discounts | Nuevo: descuentos por período y volumen |
| `dpsNewPeriodAndVolumeDiscountsDiscountGroups` | 15 | New Period And Volume Discounts Discount Groups | Nuevo: período y volumen + grupos de descuento |
| `dpsNewInactivePriceListDiscountGroups` | 16 | New Inactive Price List Discount Groups | Nuevo: lista inactiva + grupos de descuento |

## Used by (1 properties)

- [DocumentLine](../Tipos-Complejos/DocumentLine.md).`PriceSource`
