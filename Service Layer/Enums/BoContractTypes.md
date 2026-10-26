# BoContractTypes — Tipo de contrato de servicio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoContractTypes`
- **Descripción (ES):** Tipo de contrato de servicio
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ct_Customer` | 0 | Customer | Cliente |
| `ct_ItemGroup` | 1 | Item Group | Grupo de artículos |
| `ct_SerialNumber` | 2 | Serial Number | Número de serie |

## Used by (2 properties)

- [ContractTemplate](../Entidades/ContractTemplates.md).`ContractType`
- [ServiceContract](../Entidades/ServiceContracts.md).`ContractType`
