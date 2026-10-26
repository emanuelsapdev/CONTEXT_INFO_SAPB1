# BoIssueMethod — Método de emisión de componentes

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoIssueMethod`
- **Descripción (ES):** Método de emisión de componentes
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `im_Backflush` | 0 | Backflush | Notificación (backflush) |
| `im_Manual` | 1 | Manual | Manual |

## Used by (3 properties)

- [Item](../Entidades/Items.md).`IssueMethod`
- [ProductTreeLine](../Tipos-Complejos/ProductTreeLine.md).`IssueMethod`
- [ProductionOrderLine](../Tipos-Complejos/ProductionOrderLine.md).`ProductionOrderIssueType`
