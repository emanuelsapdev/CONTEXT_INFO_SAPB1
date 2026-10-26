# ProductTreeStage — Etapas de la lista de materiales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ProductTreeStage`
- **Descripción (ES):** Etapas de la lista de materiales
- **Description (EN):** Product Tree Stage
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Father` | Edm.String | Yes | Father | Padre |
| 2 | `StageID` | Edm.Int32 | Yes | Stage ID | ID de etapa |
| 3 | `SequenceNumber` | Edm.Int32 | Yes | Sequence Number | Número de secuencia |
| 4 | `StageEntry` | Edm.Int32 | Yes | Stage Entry | Entrada de la etapa |
| 5 | `Name` | Edm.String | Yes | Name | Nombre |
| 6 | `WaitingDays` | Edm.Double | Yes | Waiting Days | Días de espera |

## Used by (properties)

- [ProductTree](../Entidades/ProductTrees.md).`ProductTreeStages`
