# DunningTerms — Condiciones de reclamación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `DunningTerms`
- **Descripción (ES):** Condiciones de reclamación
- **Entity type:** `DunningTerm`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [ODUT](../../Tablas%20SAP%20B1/ODUT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 19 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/DunningTerms?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/DunningTerms/$count` | Contar |
| Get by key | `GET /b1s/v2/DunningTerms('value')` | Obtener por clave |
| Create | `POST /b1s/v2/DunningTerms` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/DunningTerms('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/DunningTerms('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/DunningTerms('value')` (only if the B1 object allows removal) | Borrar |

## Properties (19)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `GroupingMethod` | [GroupingMethodEnum](../Enums/GroupingMethodEnum.md) | Yes | Grouping Method | Método de agrupación |
| 4 | `DaysInYear` | Edm.Int32 | Yes | Days In Year | Días del año |
| 5 | `DaysInMonth` | Edm.Int32 | Yes | Days In Month | Días del mes |
| 6 | `CalculateInterestMethod` | [CalculateInterestMethodEnum](../Enums/CalculateInterestMethodEnum.md) | Yes | Calculate Interest Method | Método de cálculo de intereses |
| 7 | `ExchangeRateSelect` | [ExchangeRateSelectEnum](../Enums/ExchangeRateSelectEnum.md) | Yes | Exchange Rate Select | Selección de tipo de cambio |
| 8 | `YearlyInterestRate` | Edm.Double | Yes | Yearly Interest Rate | Tasa de interés anual |
| 9 | `LetterFee` | Edm.Double | Yes | Letter Fee | Cargo por carta |
| 10 | `LetterFeeCurrency` | Edm.String | Yes | Letter Fee Currency | Moneda del cargo por carta |
| 11 | `MinimumBalance` | Edm.Double | Yes | Minimum Balance | Saldo mínimo |
| 12 | `MinimumBalanceCurrency` | Edm.String | Yes | Minimum Balance Currency | Moneda del saldo mínimo |
| 13 | `IncludeInterest` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Interest | Incluir intereses |
| 14 | `ApplyHighestLetterTemplate` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Apply Highest Letter Template | Aplicar plantilla de carta de mayor nivel |
| 15 | `AutomaticPosting` | [AutomaticPostingEnum](../Enums/AutomaticPostingEnum.md) | Yes | Automatic Posting | Contabilización automática |
| 16 | `InterestAccount` | Edm.String | Yes | Interest Account | Cuenta de intereses |
| 17 | `FeeAccount` | Edm.String | Yes | Fee Account | Cuenta de cargos |
| 18 | `BaseDateSelect` | [BaseDateSelectEnum](../Enums/BaseDateSelectEnum.md) | Yes | Base Date Select | Selección de fecha base |
| 19 | `DunningTermLines` | Collection([DunningTermLine](../Tipos-Complejos/DunningTermLine.md)) | Yes | Dunning Term Lines | Líneas de la condición de reclamación |

## Navigation properties (2)

Use `GET /b1s/v2/DunningTerms('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | InterestAccount → Code | Plan de cuentas (cuentas de mayor) |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
