# CreditCards — Tarjetas de crédito

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `CreditCards`
- **Descripción (ES):** Tarjetas de crédito
- **Entity type:** `CreditCard` (open type: accepts dynamic/UDF properties)
- **Key:** `CreditCardCode` (Edm.Int32)
- **DB tables (main / lines):** [OCRC](../../Tablas%20SAP%20B1/OCRC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 4 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/CreditCards?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/CreditCards/$count` | Contar |
| Get by key | `GET /b1s/v2/CreditCards(1)` | Obtener por clave |
| Create | `POST /b1s/v2/CreditCards` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/CreditCards(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/CreditCards(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/CreditCards(1)` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CreditCardCode` 🔑 | Edm.Int32 | No | Credit Card Code | Código de tarjeta de crédito |
| 2 | `CreditCardName` | Edm.String | Yes | Credit Card Name | Nombre de tarjeta de crédito |
| 3 | `GLAccount` | Edm.String | Yes | G/L Account | Cuenta de mayor |
| 4 | `Telephone` | Edm.String | Yes | Telephone | Teléfono |
| 5 | `CompanyID` | Edm.String | Yes | Company ID | ID de la sociedad |
| 6 | `CountryCode` | Edm.String | Yes | Country Code | Código de país |

## Navigation properties (4)

Use `GET /b1s/v2/CreditCards(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `CreditPaymentMethods` | Collection([CreditPaymentMethod](../Entidades/CreditPaymentMethods.md)) | [CreditPaymentMethods](CreditPaymentMethods.md) |  | Vías de pago con tarjeta de crédito |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | GLAccount → Code | Plan de cuentas (cuentas de mayor) |
| `Country` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | CountryCode → Code | País |
