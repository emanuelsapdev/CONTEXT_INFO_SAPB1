# VatGroups — Grupos de impuestos (IVA)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `VatGroups`
- **Descripción (ES):** Grupos de impuestos (IVA)
- **Entity type:** `VatGroup` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OVTG](../../Tablas%20SAP%20B1/OVTG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 33 · **Navigation properties:** 10 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/VatGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/VatGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/VatGroups('value')` | Obtener por clave |
| Create | `POST /b1s/v2/VatGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/VatGroups('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/VatGroups('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/VatGroups('value')` (only if the B1 object allows removal) | Borrar |

## Properties (33)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Category` | [BoVatCategoryEnum](../Enums/BoVatCategoryEnum.md) | Yes | Category | Categoría |
| 4 | `TaxAccount` | Edm.String | Yes | Tax Account | Cuenta de impuestos |
| 5 | `EU` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | EU | Unión Europea |
| 6 | `TriangularDeal` | Edm.String | Yes | Triangular Deal | Operación triangular |
| 7 | `AcquisitionReverse` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Acquisition Reverse | Inversión de adquisición |
| 8 | `NonDeduct` | Edm.Double | Yes | Non Deduct | No deducible |
| 9 | `AcquisitionTax` | Edm.String | Yes | Acquisition Tax | Impuesto de adquisición |
| 10 | `GoodsShipment` | Edm.String | Yes | Goods Shipment | Envío de mercancías |
| 11 | `NonDeductAcc` | Edm.String | Yes | Non Deduct Account | Cuenta no deducible |
| 12 | `DeferredTaxAcc` | Edm.String | Yes | Deferred Tax Account | Cuenta de impuesto diferido |
| 13 | `Correction` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Correction | Corrección |
| 14 | `VatCorrection` | Edm.String | Yes | Vat Correction | Corrección de IVA |
| 15 | `EqualizationTaxAccount` | Edm.String | Yes | Equalization Tax Account | Cuenta de recargo de equivalencia |
| 16 | `ServiceSupply` | Edm.String | Yes | Service Supply | Prestación de servicios |
| 17 | `Inactive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inactive | Inactivo |
| 18 | `TaxTypeBlackList` | [TaxTypeBlackListEnum](../Enums/TaxTypeBlackListEnum.md) | Yes | Tax Type Black List | Lista negra de tipos de impuesto |
| 19 | `Report349Code` | [Report349CodeListEnum](../Enums/Report349CodeListEnum.md) | Yes | Report 349 Code | Código del modelo 349 |
| 20 | `VATInRevenueAccount` | Edm.String | Yes | VAT In Revenue Account | IVA en cuenta de ingresos |
| 21 | `DownPaymentTaxOffsetAccount` | Edm.String | Yes | Down Payment Tax Offset Account | Contracuenta de impuesto de anticipos |
| 22 | `CashDiscountAccount` | Edm.String | Yes | Cash Discount Account | Cuenta de descuento por pronto pago |
| 23 | `VATDeductibleAccount` | Edm.String | Yes | VAT Deductible Account | Cuenta de IVA deducible |
| 24 | `TaxRegion` | [VatGroupsTaxRegionEnum](../Enums/VatGroupsTaxRegionEnum.md) | Yes | Tax Region | Región fiscal |
| 25 | `AcquisitionReverseCorrespondingTaxCode` | Edm.String | Yes | Acquisition Reverse Corresponding Tax Code | Indicador de impuesto correspondiente a inversión de adquisición |
| 26 | `EBooksVatCategory` | Edm.Int32 | Yes | E Books Vat Category | Categoría de IVA (libros electrónicos) |
| 27 | `TaxExemptionReason` | Edm.String | Yes | Tax Exemption Reason | Motivo de exención de impuestos |
| 28 | `SAFTTaxCode` | [SAFTTaxCodeEnum](../Enums/SAFTTaxCodeEnum.md) | Yes | SAFT Tax Code | Código de impuesto SAF-T |
| 29 | `EBooksVatExemptionCause` | Edm.Int32 | Yes | E Books Vat Exemption Cause | Causa de exención de IVA (libros electrónicos) |
| 30 | `EBooksVatExpClassType` | Edm.Int32 | Yes | E Books Vat Exp Class Type | Tipo de clasificación de gastos de IVA |
| 31 | `EBooksVatExpClassCategory` | Edm.Int32 | Yes | E Books Vat Exp Class Category | Categoría de clasificación de gastos de IVA |
| 32 | `SAFTTaxCodeEx` | Edm.String | Yes | SAFT Tax Code Ex | Código de impuesto SAF-T (ampliado) |
| 33 | `VatGroups_Lines` | Collection([VatGroups_Line](../Tipos-Complejos/VatGroups_Line.md)) | Yes | Vat Groups Lines | Líneas de grupos de IVA |

## Navigation properties (10)

Use `GET /b1s/v2/VatGroups('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | TaxAccount → Code | Plan de cuentas (cuentas de mayor) |
| `TaxExemptReason` | [TaxExemptReason](../Entidades/TaxExemptReasons.md) | [TaxExemptReasons](TaxExemptReasons.md) | TaxExemptionReason → Code | Motivos de exención de impuestos |
| `VendorPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [VendorPayments](VendorPayments.md) |  | Pagos efectuados |
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `GLAccountAdvancedRules` | Collection([GLAccountAdvancedRule](../Entidades/GLAccountAdvancedRules.md)) | [GLAccountAdvancedRules](GLAccountAdvancedRules.md) |  | Reglas avanzadas de cuentas de mayor |
| `AdditionalExpenses` | Collection([AdditionalExpense](../Entidades/AdditionalExpenses.md)) | [AdditionalExpenses](AdditionalExpenses.md) |  | Gastos adicionales (fletes) |
| `PaymentDrafts` | Collection([Payment](../Entidades/VendorPayments.md)) | [PaymentDrafts](PaymentDrafts.md) |  | Borradores de pagos |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
| `IncomingPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [IncomingPayments](IncomingPayments.md) |  | Pagos recibidos |
| `Deposits` | Collection([Deposit](../Entidades/Deposits.md)) | [Deposits](Deposits.md) |  | Depósitos |
