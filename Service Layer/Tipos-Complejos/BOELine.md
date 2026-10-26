# BOELine — Líneas de letras de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BOELine`
- **Descripción (ES):** Líneas de letras de cambio
- **Description (EN):** BOE Line

- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BOEKey` | Edm.Int32 | Yes | BOE Key | Clave de letra de cambio |
| 2 | `BOENumber` | Edm.Int32 | Yes | BOE Number | Número de letra de cambio |
| 3 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 4 | `Bank` | Edm.String | Yes | Bank | Banco |
| 5 | `Branch` | Edm.String | Yes | Branch | Sucursal |
| 6 | `AccountNumber` | Edm.String | Yes | Account Number | Número de cuenta |
| 7 | `Amount` | Edm.Double | Yes | Amount | Importe |
| 8 | `BOEStatus` | [BoBoeStatus](../Enums/BoBoeStatus.md) | Yes | BOE Status | Estado de letra de cambio |
| 9 | `Transferred` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Transferred | Transferido |

## Used by (properties)

- [Deposit](../Entidades/Deposits.md).`BOELines`

## Used by (service operations)

- [`BOELinesService_GetBOELine`](../Servicios/BOELinesService.md#boelinesservice_getboeline)
