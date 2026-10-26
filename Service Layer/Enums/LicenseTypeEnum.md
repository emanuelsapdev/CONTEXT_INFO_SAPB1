# LicenseTypeEnum — Tipo de licencia

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `LicenseTypeEnum`
- **Descripción (ES):** Tipo de licencia
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `lkIdirect` | 25 | Idirect | Indirecta |
| `lkSOAIndirect` | 20 | SOA Indirect | SOA indirecta |
| `lkSOA` | 21 | SOA | SOA |
| `lkB1iIndirect` | 22 | B 1i Indirect | B1i indirecta |
| `lkB1i` | 23 | B 1i | B1i |

## Used by (1 properties)

- [UpdateUserLicenseParams](../Tipos-Complejos/UpdateUserLicenseParams.md).`LicenseType`
