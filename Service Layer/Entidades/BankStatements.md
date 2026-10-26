# BankStatements — Extractos bancarios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BankStatements`
- **Descripción (ES):** Extractos bancarios
- **Entity type:** `BankStatement`
- **Key:** `InternalNumber` (Edm.Int32)
- **DB tables (main / lines):** [OBNH](../../Tablas%20SAP%20B1/OBNH.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 14 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BankStatements?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BankStatements/$count` | Contar |
| Get by key | `GET /b1s/v2/BankStatements(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BankStatements` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BankStatements(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BankStatements(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BankStatements(1)` (only if the B1 object allows removal) | Borrar |

## Properties (14)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `InternalNumber` 🔑 | Edm.Int32 | No | Internal Number | Número interno |
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
| 12 | `BankStatementFileHash` | Edm.String | Yes | Bank Statement File Hash | Hash del archivo del extracto bancario |
| 13 | `BankStatementGUID` | Edm.String | Yes | Bank Statement GUID | GUID del extracto bancario |
| 14 | `BankStatementRows` | Collection([BankStatementRow](../Tipos-Complejos/BankStatementRow.md)) | Yes | Bank Statement Rows | Líneas del extracto bancario |

## Navigation properties (2)

Use `GET /b1s/v2/BankStatements(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `HouseBankAccount` | [HouseBankAccount](../Entidades/HouseBankAccounts.md) | [HouseBankAccounts](HouseBankAccounts.md) | BankAccountKey → AbsoluteEntry | Cuenta bancaria propia |
| `Currency2` | [Currency](../Entidades/Currencies.md) | [Currencies](Currencies.md) | Currency → Code | Monedas |
