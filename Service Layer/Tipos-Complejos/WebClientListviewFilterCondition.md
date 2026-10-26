# WebClientListviewFilterCondition — Condiciones del filtro de vista de lista

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WebClientListviewFilterCondition`
- **Descripción (ES):** Condiciones del filtro de vista de lista
- **Description (EN):** Web Client Listview Filter Condition

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` | Edm.String | Yes | Guid | GUID |
| 2 | `Order` | Edm.Int32 | Yes | Order | Pedido / orden |
| 3 | `ColumnName` | Edm.String | Yes | Column Name | Nombre de columna |
| 4 | `CompareExpression` | Edm.String | Yes | Compare Expression | Expresión de comparación |
| 5 | `Value` | Edm.String | Yes | Value | Valor |

## Used by (properties)

- [WebClientListviewFilter](../Entidades/WebClientListviewFilters.md).`WebClientListviewFilterConditions`
