# BoResolutionUnits — Unidad de tiempo de resolución

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoResolutionUnits`
- **Descripción (ES):** Unidad de tiempo de resolución
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rsu_Days` | 0 | Days | Días |
| `rsu_Hours` | 1 | Hours | Horas |

## Used by (3 properties)

- [ContractTemplate](../Entidades/ContractTemplates.md).`ResolutionUnit`
- [CustomerEquipmentCard](../Entidades/CustomerEquipmentCards.md).`RequiredResolutionUnit`
- [ServiceContract](../Entidades/ServiceContracts.md).`ResolutionUnit`
