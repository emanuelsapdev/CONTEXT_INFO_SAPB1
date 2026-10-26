# AttributeGroupLine — Línea de grupo de atributos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AttributeGroupLine`
- **Descripción (ES):** Línea de grupo de atributos
- **Description (EN):** Attribute Group Line

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.Int32 | Yes | Code | Código |
| 2 | `SortNumber` | Edm.Int32 | Yes | Sort Number | Número de orden |
| 3 | `AttributeID` | Edm.Int32 | Yes | Attribute ID | ID de atributo |
| 4 | `AttributeName` | Edm.String | Yes | Attribute Name | Nombre del atributo |
| 5 | `FieldType` | [AttributeGroupFieldTypeEnum](../Enums/AttributeGroupFieldTypeEnum.md) | Yes | Field Type | Tipo de campo |
| 6 | `DefaultValue` | Edm.String | Yes | Default Value | Valor predeterminado |

## Used by (properties)

- [AttributeGroup](../Entidades/AttributeGroups.md).`AttributeGroupCollection`
