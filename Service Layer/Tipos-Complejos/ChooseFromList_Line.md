# ChooseFromList_Line — Líneas de selección de lista

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ChooseFromList_Line`
- **Descripción (ES):** Líneas de selección de lista
- **Description (EN):** Choose From List Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ObjectName` | Edm.String | Yes | Object Name | Nombre del objeto |
| 2 | `FieldIndex` | Edm.Int32 | Yes | Field Index | Índice del campo |
| 3 | `FieldNo` | Edm.String | Yes | Field Number | Número del campo |
| 4 | `DisplayedName` | Edm.String | Yes | Displayed Name | Nombre mostrado |
| 5 | `GroupBy` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Group By | Agrupar por |
| 6 | `Visible` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Visible | Visible |
| 7 | `ShowType` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Show Type | Tipo de visualización |
| 8 | `SortOrder` | [SortOrderEnum](../Enums/SortOrderEnum.md) | Yes | Sort Order | Orden |
| 9 | `VisualIndex` | Edm.Int32 | Yes | Visual Index | Índice visual |

## Used by (properties)

- [ChooseFromList](../Entidades/ChooseFromList.md).`ChooseFromList_Lines`
