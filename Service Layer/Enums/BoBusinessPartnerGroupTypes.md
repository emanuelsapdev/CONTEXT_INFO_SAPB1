# BoBusinessPartnerGroupTypes — Tipo de grupo de socios de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoBusinessPartnerGroupTypes`
- **Descripción (ES):** Tipo de grupo de socios de negocios
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bbpgt_CustomerGroup` | 0 | Customer Group | Grupo de clientes |
| `bbpgt_VendorGroup` | 1 | Vendor Group | Grupo de proveedores |

## Used by (1 properties)

- [BusinessPartnerGroup](../Entidades/BusinessPartnerGroups.md).`Type`
