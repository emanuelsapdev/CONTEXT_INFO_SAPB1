# TaxCodeDeterminationTCDTypeEnum — Tipo de determinación TCD

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `TaxCodeDeterminationTCDTypeEnum`
- **Descripción (ES):** Tipo de determinación TCD
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `tcdtMaterialItem` | 0 | Material Item | Artículo material |
| `tcdtServiceItem` | 1 | Service Item | Artículo de servicio |
| `tcdtServiceDocument` | 2 | Service Document | Documento de servicio |
| `tcdtWithholdingTax` | 3 | Withholding Tax | Retención de impuestos |

## Used by (1 properties)

- [TaxCodeDeterminationTCD](../Entidades/TaxCodeDeterminationsTCD.md).`TcdType`
