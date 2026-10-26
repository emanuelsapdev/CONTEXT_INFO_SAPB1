# ItemProject — Proyectos del artículo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ItemProject`
- **Descripción (ES):** Proyectos del artículo
- **Description (EN):** Item Project

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `ValidFrom` | Edm.DateTimeOffset | Yes | Valid From | Válido desde |
| 3 | `ValidTo` | Edm.DateTimeOffset | Yes | Valid To | Válido hasta |
| 4 | `Project` | Edm.String | Yes | Project | Proyecto |

## Used by (properties)

- [Item](../Entidades/Items.md).`ItemProjects`
