# BankStatementsFilter — Filtro de extractos bancarios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BankStatementsFilter`
- **Descripción (ES):** Filtro de extractos bancarios
- **Description (EN):** Bank Statements Filter

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Country` | Edm.String | Yes | Country | País |
| 2 | `Bank` | Edm.String | Yes | Bank | Banco |
| 3 | `Account` | Edm.String | Yes | Account | Cuenta |

## Used by (service operations)

- [`BankStatementsService_GetBankStatementList`](../Servicios/BankStatementsService.md#bankstatementsservice_getbankstatementlist)
