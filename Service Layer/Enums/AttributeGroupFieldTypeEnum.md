# AttributeGroupFieldTypeEnum — Tipo de campo del grupo de atributos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `AttributeGroupFieldTypeEnum`
- **Descripción (ES):** Tipo de campo del grupo de atributos
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `agftText` | 0 | Text | Texto |
| `agftNumeric` | 1 | Numeric | Numérico |
| `agftDate` | 2 | Date | Fecha |
| `agftAmount` | 3 | Amount | Importe |
| `agftPrice` | 4 | Price | Precio |
| `agftQuantity` | 5 | Quantity | Cantidad |

## Used by (1 properties)

- [AttributeGroupLine](../Tipos-Complejos/AttributeGroupLine.md).`FieldType`
