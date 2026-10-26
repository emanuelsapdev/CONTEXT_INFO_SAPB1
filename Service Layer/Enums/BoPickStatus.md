# BoPickStatus — Estado de la lista de picking

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoPickStatus`
- **Descripción (ES):** Estado de la lista de picking
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ps_Released` | 0 | Released | Liberado |
| `ps_Picked` | 1 | Picked | Pickeado |
| `ps_PartiallyPicked` | 2 | Partially Picked | Parcialmente pickeado |
| `ps_PartiallyDelivered` | 3 | Partially Delivered | Parcialmente entregado |
| `ps_Closed` | 4 | Closed | Cerrado |

## Used by (2 properties)

- [PickList](../Entidades/PickLists.md).`Status`
- [PickListsLine](../Tipos-Complejos/PickListsLine.md).`PickStatus`
