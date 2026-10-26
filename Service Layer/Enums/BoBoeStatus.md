# BoBoeStatus — Estado de la letra de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoBoeStatus`
- **Descripción (ES):** Estado de la letra de cambio
- **Underlying type:** Edm.Int32
- **Members:** 7

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `boes_Created` | 0 | Created | Creada |
| `boes_Sent` | 1 | Sent | Enviada |
| `boes_Deposited` | 2 | Deposited | Depositada |
| `boes_Paid` | 3 | Paid | Pagada |
| `boes_Cancelled` | 4 | Cancelled | Cancelada |
| `boes_Closed` | 5 | Closed | Cerrada |
| `boes_Failed` | 6 | Failed | Fallida |

## Used by (6 properties)

- [BOELine](../Tipos-Complejos/BOELine.md).`BOEStatus`
- [OccurenceCode](../Entidades/OccurrenceCodes.md).`RequestedBoeStatus`
- [OccurenceCodeParams](../Tipos-Complejos/OccurenceCodeParams.md).`RequestedBoeStatus`
- [Payment](../Entidades/VendorPayments.md).`BillofExchangeStatus`
- [RetornoCode](../Entidades/RetornoCodes.md).`BoeStatus`
- [RetornoCodeParams](../Tipos-Complejos/RetornoCodeParams.md).`BoeStatus`
