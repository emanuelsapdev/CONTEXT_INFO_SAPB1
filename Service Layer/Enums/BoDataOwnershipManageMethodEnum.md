# BoDataOwnershipManageMethodEnum — Método de gestión de propiedad de datos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoDataOwnershipManageMethodEnum`
- **Descripción (ES):** Método de gestión de propiedad de datos
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `doManageByDocOnly` | 0 | Manage By Document Only | Solo por documento |
| `doManageByBPOnly` | 1 | Manage By Business Partner Only | Solo por socio de negocios |
| `doManageByBPnDoc` | 2 | Manage By B Pn Document | Por socio de negocios y documento |
| `doManageByBranch` | 3 | Manage By Branch | Por sucursal |

## Used by (1 properties)

- [AdminInfo](../Tipos-Complejos/AdminInfo.md).`DataOwnershipManageBy`
