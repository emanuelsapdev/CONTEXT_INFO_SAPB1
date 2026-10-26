# ResourceCapacitySourceTypeEnum — Tipo de origen de capacidad del recurso

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ResourceCapacitySourceTypeEnum`
- **Descripción (ES):** Tipo de origen de capacidad del recurso
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rcstNone` | 0 | None | Ninguno |
| `rcstProductionOrder` | 202 | Production Order | Orden de fabricación |
| `rcstIssueForProduction` | 60 | Issue For Production | Emisión para producción |
| `rcstReceiptFromProduction` | 59 | Receipt From Production | Recibo de producción |

## Used by (2 properties)

- [ResourceCapacity](../Entidades/ResourceCapacities.md).`SourceType`
- [ResourceCapacityParams](../Tipos-Complejos/ResourceCapacityParams.md).`SourceType`
