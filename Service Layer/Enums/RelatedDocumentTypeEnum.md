# RelatedDocumentTypeEnum — Tipo de documento relacionado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `RelatedDocumentTypeEnum`
- **Descripción (ES):** Tipo de documento relacionado
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rdt_Payment` | 24 | Payment | Pago |
| `rdt_Reconciliation` | 321 | Reconciliation | Conciliación |

## Used by (2 properties)

- [RelatedDocument](../Tipos-Complejos/RelatedDocument.md).`DocTye`
- [RelatedDocument](../Tipos-Complejos/RelatedDocument.md).`DocType`
