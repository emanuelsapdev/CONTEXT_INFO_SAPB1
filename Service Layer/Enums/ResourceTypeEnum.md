# ResourceTypeEnum — Tipo de recurso

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ResourceTypeEnum`
- **Descripción (ES):** Tipo de recurso
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rtMachine` | 0 | Machine | Máquina |
| `rtLabor` | 1 | Labor | Mano de obra |
| `rtOther` | 2 | Other | Otro |

## Used by (2 properties)

- [Resource](../Entidades/Resources.md).`Type`
- [ResourceGroup](../Entidades/ResourceGroups.md).`Type`
