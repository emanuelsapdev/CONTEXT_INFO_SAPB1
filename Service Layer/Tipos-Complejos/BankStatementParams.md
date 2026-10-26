# BankStatementParams — Parámetros de extractos bancarios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BankStatementParams`
- **Descripción (ES):** Parámetros de extractos bancarios
- **Description (EN):** Bank Statement Parameters

- **Properties:** 11

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `InternalNumber` | Edm.Int32 | Yes | Internal Number | Número interno |
| 2 | `BankAccountKey` | Edm.Int32 | Yes | Bank Account Key | Clave de la cuenta bancaria |
| 3 | `StatementNumber` | Edm.String | Yes | Statement Number | Número del extracto |
| 4 | `StatementDate` | Edm.DateTimeOffset | Yes | Statement Date | Fecha del extracto |
| 5 | `Status` | [BankStatementStatusEnum](../Enums/BankStatementStatusEnum.md) | Yes | Status | Estado |
| 6 | `Imported` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Imported | Importado |
| 7 | `StartingBalanceF` | Edm.Double | Yes | Starting Balance F | Saldo inicial (ME) |
| 8 | `EndingBalanceF` | Edm.Double | Yes | Ending Balance F | Saldo final (ME) |
| 9 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 10 | `StartingBalanceL` | Edm.Double | Yes | Starting Balance L | Saldo inicial (moneda local) |
| 11 | `EndingBalanceL` | Edm.Double | Yes | Ending Balance L | Saldo final (moneda local) |

## Used by (service operations)

- [`BankStatementsService_GetBankStatementList`](../Servicios/BankStatementsService.md#bankstatementsservice_getbankstatementlist)
