# CheckLine — Líneas de cheques

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CheckLine`
- **Descripción (ES):** Líneas de cheques
- **Description (EN):** Check Line

- **Properties:** 15

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CheckKey` | Edm.Int32 | Yes | Check Key | Clave del cheque |
| 2 | `CheckNumber` | Edm.Int32 | Yes | Check Number | Número de cheque |
| 3 | `Bank` | Edm.String | Yes | Bank | Banco |
| 4 | `Branch` | Edm.String | Yes | Branch | Sucursal |
| 5 | `CashCheck` | Edm.String | Yes | Cash Check | Cheque de caja |
| 6 | `CheckDate` | Edm.DateTimeOffset | Yes | Check Date | Fecha del cheque |
| 7 | `Customer` | Edm.String | Yes | Customer | Cliente |
| 8 | `CheckAmount` | Edm.Double | Yes | Check Amount | Importe del cheque |
| 9 | `Deposited` | [BoDepositCheckEnum](../Enums/BoDepositCheckEnum.md) | Yes | Deposited | Depositado |
| 10 | `Transferred` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Transferred | Transferido |
| 11 | `AccountNumber` | Edm.String | Yes | Account Number | Número de cuenta |
| 12 | `CheckCurrency` | Edm.String | Yes | Check Currency | Moneda del cheque |
| 13 | `FiscalID` | Edm.String | Yes | Fiscal ID | ID fiscal |
| 14 | `OriginallyIssuedBy` | Edm.String | Yes | Originally Issued By | Emitido originalmente por |
| 15 | `RejectedByBank` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Rejected By Bank | Rechazado por el banco |

## Used by (properties)

- [Deposit](../Entidades/Deposits.md).`CheckLines`

## Used by (service operations)

- [`CheckLinesService_GetCheckLine`](../Servicios/CheckLinesService.md#checklinesservice_getcheckline)
