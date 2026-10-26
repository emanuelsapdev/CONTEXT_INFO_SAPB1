# BillOfExchangeTransDeposit — Depósitos de transacción de letras de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BillOfExchangeTransDeposit`
- **Descripción (ES):** Depósitos de transacción de letras de cambio
- **Description (EN):** Bill Of Exchange Trans Deposit
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DepositNorm` | Edm.String | Yes | Deposit Norm | Norma del depósito |
| 2 | `PostingType` | [BoDepositPostingTypes](../Enums/BoDepositPostingTypes.md) | Yes | Posting Type | Tipo de contabilización |
| 3 | `BankCountry` | Edm.String | Yes | Bank Country | País del banco |
| 4 | `BankAccount` | Edm.String | Yes | Bank Account | Cuenta bancaria |
| 5 | `BankDepositAccount` | Edm.String | Yes | Bank Deposit Account | Cuenta de depósito bancario |
| 6 | `BankBranch` | Edm.String | Yes | Bank Branch | Sucursal bancaria |

## Used by (properties)

- [BillOfExchangeTransaction](../Entidades/BillOfExchangeTransactions.md).`BillOfExchangeTransDeposits`
