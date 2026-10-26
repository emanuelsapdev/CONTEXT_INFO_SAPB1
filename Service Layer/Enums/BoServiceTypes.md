# BoServiceTypes — Tipo de servicio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoServiceTypes`
- **Descripción (ES):** Tipo de servicio
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bst_Regular` | 0 | Regular | Regular |
| `bst_Warranty` | 1 | Warranty | Garantía |

## Used by (1 properties)

- [ServiceContract](../Entidades/ServiceContracts.md).`ServiceType`
