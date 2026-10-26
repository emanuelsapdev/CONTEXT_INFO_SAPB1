# BoCardCompanyTypes — Tipo de entidad del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoCardCompanyTypes`
- **Descripción (ES):** Tipo de entidad del socio de negocios
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `cCompany` | 0 | Company | Empresa (C) |
| `cPrivate` | 1 | Private | Privado (I) |
| `cGovernment` | 2 | Government | Gobierno (G) |
| `cEmployee` | 3 | Employee | Empleado (E) |

## Used by (1 properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`CompanyPrivate`
