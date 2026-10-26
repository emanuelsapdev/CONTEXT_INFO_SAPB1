# AmountCatTypeEnum — Tipo de categoría de importe

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `AmountCatTypeEnum`
- **Descripción (ES):** Tipo de categoría de importe
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `act_Open` | 0 | Open | Abierto |
| `act_Invoiced` | 1 | Invoiced | Facturado |

## Used by (2 properties)

- [PMS_DocumentData](../Tipos-Complejos/PMS_DocumentData.md).`AmountCategory`
- [PM_DocumentData](../Tipos-Complejos/PM_DocumentData.md).`AmountCategory`
