# EDocGenerationTypeEnum — Tipo de generación del documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `EDocGenerationTypeEnum`
- **Descripción (ES):** Tipo de generación del documento electrónico
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `edocGenerate` | 0 | Generate | Generar |
| `edocGenerateLater` | 1 | Generate Later | Generar más tarde |
| `edocNotRelevant` | 2 | Not Relevant | No relevante |

## Used by (2 properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`EDocGenerationType`
- [Document](../Entidades/PurchaseQuotations.md).`EDocGenerationType`
