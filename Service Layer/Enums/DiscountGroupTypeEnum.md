# DiscountGroupTypeEnum — Tipo de grupo de descuento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `DiscountGroupTypeEnum`
- **Descripción (ES):** Tipo de grupo de descuento
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `dgt_AllBPs` | 0 | All B Ps | Todos los socios de negocios |
| `dgt_CustomerGroup` | 1 | Customer Group | Grupo de clientes |
| `dgt_VendorGroup` | 2 | Vendor Group | Grupo de proveedores |
| `dgt_SpecificBP` | 3 | Specific Business Partner | Socio de negocios específico |

## Used by (2 properties)

- [EnhancedDiscountGroup](../Entidades/EnhancedDiscountGroups.md).`Type`
- [EnhancedDiscountGroupParams](../Tipos-Complejos/EnhancedDiscountGroupParams.md).`Type`
