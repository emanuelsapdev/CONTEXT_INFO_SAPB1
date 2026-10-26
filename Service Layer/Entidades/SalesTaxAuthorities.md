# SalesTaxAuthorities — Autoridades del impuesto sobre ventas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SalesTaxAuthorities`
- **Descripción (ES):** Autoridades del impuesto sobre ventas
- **Entity type:** `SalesTaxAuthority` (open type: accepts dynamic/UDF properties)
- **Key:** `Type` (Edm.Int32), `Code` (Edm.String)
- **DB tables (main / lines):** [OSTA](../../Tablas%20SAP%20B1/OSTA.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 28 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SalesTaxAuthorities?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SalesTaxAuthorities/$count` | Contar |
| Get by key | `GET /b1s/v2/SalesTaxAuthorities(Type=1,Code='value')` | Obtener por clave |
| Create | `POST /b1s/v2/SalesTaxAuthorities` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SalesTaxAuthorities(Type=1,Code='value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SalesTaxAuthorities(Type=1,Code='value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/SalesTaxAuthorities(Type=1,Code='value')` (only if the B1 object allows removal) | Borrar |

## Properties (28)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `UseTaxAccount` | Edm.String | Yes | Use Tax Account | Cuenta de impuesto de uso |
| 2 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 3 | `Type` 🔑 | Edm.Int32 | No | Type | Tipo |
| 4 | `AOrRTaxAccount` | Edm.String | Yes | A Or R Tax Account | Cuenta de impuesto A o R |
| 5 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |
| 6 | `AOrPTaxAccount` | Edm.String | Yes | A Or P Tax Account | Cuenta de impuesto A o P |
| 7 | `NonDeductiblePrecent` | Edm.Double | Yes | Non Deductible Precent | Porcentaje no deducible |
| 8 | `NonDeductibleAccount` | Edm.String | Yes | Non Deductible Account | Cuenta no deducible |
| 9 | `Name` | Edm.String | Yes | Name | Nombre |
| 10 | `DeferredTaxAccount` | Edm.String | Yes | Deferred Tax Account | Cuenta de impuesto diferido |
| 11 | `Code` 🔑 | Edm.String | No | Code | Código |
| 12 | `MinTaxableAmount` | Edm.Double | Yes | Min Taxable Amount | Importe imponible mínimo |
| 13 | `MaxTaxableAmount` | Edm.Double | Yes | Max Taxable Amount | Importe imponible máximo |
| 14 | `FlatTaxAmount` | Edm.Double | Yes | Flat Tax Amount | Importe de impuesto fijo |
| 15 | `InclInPrice` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Incl In Price | Incluido en el precio |
| 16 | `Exempt` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Exempt | Exento |
| 17 | `APExpAccount` | Edm.String | Yes | AP Exp Account | Cuenta de gastos (compras) |
| 18 | `ARExpAccount` | Edm.String | Yes | AR Exp Account | Cuenta de gastos (ventas) |
| 19 | `InclInGrossRevenue` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Incl In Gross Revenue | Incluir en ingresos brutos |
| 20 | `TextCode` | Edm.Int32 | Yes | Text Code | Código de texto |
| 21 | `InclInFirstInstallment` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Incl In First Installment | Incluir en la primera cuota |
| 22 | `ReverseChargePercent` | Edm.Double | Yes | Reverse Charge Percent | Porcentaje de inversión del sujeto pasivo |
| 23 | `SalesTaxRCMAccount` | Edm.String | Yes | Sales Tax RCM Account | Cuenta RCM del impuesto sobre ventas |
| 24 | `SalesTaxRCMClrAccount` | Edm.String | Yes | Sales Tax RCM Clr Account | Cuenta de compensación RCM del impuesto sobre ventas |
| 25 | `VATExemption` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | VAT Exemption | Exención de IVA |
| 26 | `VATExemptionBasePercent` | Edm.Double | Yes | VAT Exemption Base Percent | Porcentaje base de exención de IVA |
| 27 | `VATExemptionPercent` | Edm.Double | Yes | VAT Exemption Percent | Porcentaje de exención de IVA |
| 28 | `TaxDefinitions` | Collection([TaxDefinition](../Tipos-Complejos/TaxDefinition.md)) | Yes | Tax Definitions | Definiciones de impuestos |

## Navigation properties (3)

Use `GET /b1s/v2/SalesTaxAuthorities(Type=1,Code='value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | UseTaxAccount → Code | Plan de cuentas (cuentas de mayor) |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | UserSignature → InternalKey | Usuario |
| `SalesTaxAuthoritiesType` | [SalesTaxAuthoritiesType](../Entidades/SalesTaxAuthoritiesTypes.md) | [SalesTaxAuthoritiesTypes](SalesTaxAuthoritiesTypes.md) | Type → Numerator | Tipos de autoridades del impuesto sobre ventas |
