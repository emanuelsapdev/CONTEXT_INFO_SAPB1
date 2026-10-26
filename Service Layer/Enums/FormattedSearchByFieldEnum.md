# FormattedSearchByFieldEnum — Disparador de búsqueda formateada

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `FormattedSearchByFieldEnum`
- **Descripción (ES):** Disparador de búsqueda formateada
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `fsbfWhenExitingAlteredColumn` | 0 | When Exiting Altered Column | Al salir de una columna modificada |
| `fsbfWhenFieldChanges` | 1 | When Field Changes | Cuando cambia el campo |
| `fsbfWhenColumnValueChanges` | 2 | When Column Value Changes | Cuando cambia el valor de la columna |

## Used by (1 properties)

- [FormattedSearch](../Entidades/FormattedSearches.md).`ByFieldEx`
