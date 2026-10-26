# WebClientVariants — Cliente web - Variantes

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WebClientVariants`
- **Descripción (ES):** Cliente web - Variantes
- **Entity type:** `WebClientVariant`
- **Key:** `Guid` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 22 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WebClientVariants?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WebClientVariants/$count` | Contar |
| Get by key | `GET /b1s/v2/WebClientVariants('value')` | Obtener por clave |
| Create | `POST /b1s/v2/WebClientVariants` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WebClientVariants('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WebClientVariants('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/WebClientVariants('value')` (only if the B1 object allows removal) | Borrar |

## Properties (22)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` 🔑 | Edm.String | No | Guid | GUID |
| 2 | `Order` | Edm.Int32 | Yes | Order | Pedido / orden |
| 3 | `UserId` | Edm.Int32 | Yes | User ID | ID de usuario |
| 4 | `ViewType` | Edm.String | Yes | View Type | Tipo de vista |
| 5 | `SubViewType` | Edm.String | Yes | Sub View Type | Tipo de subvista |
| 6 | `ViewId` | Edm.String | Yes | View ID | ID de vista |
| 7 | `ObjectName` | Edm.String | Yes | Object Name | Nombre del objeto |
| 8 | `FilterBarLayout` | Edm.String | Yes | Filter Bar Layout | Diseño de la barra de filtros |
| 9 | `SystemFilter` | Edm.String | Yes | System Filter | Filtro del sistema |
| 10 | `UserFilter` | Edm.String | Yes | User Filter | Filtro de usuario |
| 11 | `ConditionFilter` | Edm.String | Yes | Condition Filter | Filtro de condición |
| 12 | `IsPublic` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Public | Es público |
| 13 | `IsSystem` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is System | Es del sistema |
| 14 | `Name` | Edm.String | Yes | Name | Nombre |
| 15 | `Version` | Edm.Int32 | Yes | Version | Versión |
| 16 | `OverviewCustomization` | Edm.String | Yes | Overview Customization | Personalización de la vista general |
| 17 | `ChartCustomization` | Edm.String | Yes | Chart Customization | Personalización del gráfico |
| 18 | `WebClientVariantSelectedColumnCollection` | Collection([WebClientVariantSelectedColumn](../Tipos-Complejos/WebClientVariantSelectedColumn.md)) | Yes | Web Client Variant Selected Column Collection | Colección de columnas seleccionadas de la variante |
| 19 | `WebClientVariantGroupByCollection` | Collection([WebClientVariantGroupBy](../Tipos-Complejos/WebClientVariantGroupBy.md)) | Yes | Web Client Variant Group By Collection | Colección de agrupaciones de la variante |
| 20 | `WebClientVariantSortByCollection` | Collection([WebClientVariantSortBy](../Tipos-Complejos/WebClientVariantSortBy.md)) | Yes | Web Client Variant Sort By Collection | Colección de ordenamientos de la variante |
| 21 | `WebClientVariantEmbeddedChartCollection` | Collection([WebClientVariantEmbeddedChart](../Tipos-Complejos/WebClientVariantEmbeddedChart.md)) | Yes | Web Client Variant Embedded Chart Collection | Colección de gráficos incrustados de la variante |
| 22 | `WebClientVariantMChartCollection` | Collection([WebClientVariantMChart](../Tipos-Complejos/WebClientVariantMChart.md)) | Yes | Web Client Variant M Chart Collection | Colección de gráficos M de la variante |
