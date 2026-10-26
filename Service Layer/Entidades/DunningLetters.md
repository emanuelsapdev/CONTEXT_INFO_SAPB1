# DunningLetters — Cartas de reclamación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `DunningLetters`
- **Descripción (ES):** Cartas de reclamación
- **Entity type:** `DunningLetter` (open type: accepts dynamic/UDF properties)
- **Key:** `RowNumber` (Edm.Int32)
- **DB tables (main / lines):** [ODUN](../../Tablas%20SAP%20B1/ODUN.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 8 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/DunningLetters?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/DunningLetters/$count` | Contar |
| Get by key | `GET /b1s/v2/DunningLetters(1)` | Obtener por clave |
| Create | `POST /b1s/v2/DunningLetters` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/DunningLetters(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/DunningLetters(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/DunningLetters(1)` (only if the B1 object allows removal) | Borrar |

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FeeCurrency` | Edm.String | Yes | Fee Currency | Moneda de cargos |
| 2 | `RowNumber` 🔑 | Edm.Int32 | No | Row Number | Número de línea |
| 3 | `LetterFormat` | Edm.String | Yes | Letter Format | Formato de carta |
| 4 | `Effectiveafter` | Edm.String | Yes | Effectiveafter | Vigente después de |
| 5 | `MinimumBalanceCurrency` | Edm.String | Yes | Minimum Balance Currency | Moneda del saldo mínimo |
| 6 | `Feeperletter` | Edm.Double | Yes | Feeperletter | Cargo por carta |
| 7 | `CalcInterest` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Calc Interest | Calcular intereses |
| 8 | `MinimumBalance` | Edm.Double | Yes | Minimum Balance | Saldo mínimo |

## Navigation properties (1)

Use `GET /b1s/v2/DunningLetters(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
