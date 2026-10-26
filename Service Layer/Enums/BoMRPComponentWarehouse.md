# BoMRPComponentWarehouse — Almacén de componentes en MRP

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoMRPComponentWarehouse`
- **Descripción (ES):** Almacén de componentes en MRP
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bomcw_BOM` | 0 | BOM | Desde la lista de materiales |
| `bomcw_Parent` | 1 | Parent | Del artículo padre |

## Used by (2 properties)

- [Item](../Entidades/Items.md).`ComponentWarehouse`
- [ItemGroups](../Entidades/ItemGroups.md).`ComponentWarehouse`
