# SpecificWTHAmountsService — Importes de retención específicos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SpecificWTHAmountsService`
- **Descripción (ES):** Importes de retención específicos
- **Entity type:** `SpecificWTHAmounts` (open type: accepts dynamic/UDF properties)
- **Key:** `PaymentReasonCode` (Edm.String), `CardCode` (Edm.String), `CUSplit` (BoYesNoEnum)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 63 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SpecificWTHAmountsService?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SpecificWTHAmountsService/$count` | Contar |
| Get by key | `GET /b1s/v2/SpecificWTHAmountsService(PaymentReasonCode='value',CardCode='value',CUSplit='value')` | Obtener por clave |
| Create | `POST /b1s/v2/SpecificWTHAmountsService` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SpecificWTHAmountsService(PaymentReasonCode='value',CardCode='value',CUSplit='value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SpecificWTHAmountsService(PaymentReasonCode='value',CardCode='value',CUSplit='value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/SpecificWTHAmountsService(PaymentReasonCode='value',CardCode='value',CUSplit='value')` (only if the B1 object allows removal) | Borrar |

## Properties (63)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PaymentReasonCode` 🔑 | Edm.String | No | Payment Reason Code | Código de motivo de pago |
| 2 | `CardCode` 🔑 | Edm.String | No | Card Code | Código del socio de negocios |
| 3 | `CUSplit` 🔑 | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | No | CU Split | División CU |
| 4 | `FullWtaxTaxationInAdvance` | Edm.Double | Yes | Full Wtax Taxation In Advance | Retención total por adelantado |
| 5 | `WTaxAmountOnHold` | Edm.Double | Yes | W Tax Amount On Hold | Importe de retención retenido |
| 6 | `RegionalIRPEFHeldAsWTax` | Edm.Double | Yes | Regional IRPEF Held As W Tax | IRPEF regional retenido como retención |
| 7 | `RegionalIRPEFInAdvance` | Edm.Double | Yes | Regional IRPEF In Advance | IRPEF regional por adelantado |
| 8 | `RegionalSuspendedTaxIRPEF` | Edm.Double | Yes | Regional Suspended Tax IRPEF | IRPEF regional suspendido |
| 9 | `MunicipalTaxAsWTaxIRPEF` | Edm.Double | Yes | Municipal Tax As W Tax IRPEF | Impuesto municipal como retención IRPEF |
| 10 | `MunicipalTaxHeldAsAdvance` | Edm.Double | Yes | Municipal Tax Held As Advance | Impuesto municipal retenido como anticipo |
| 11 | `SuspendedMunicipalTax` | Edm.Double | Yes | Suspended Municipal Tax | Impuesto municipal suspendido |
| 12 | `TaxableAmtPreviousYear` | Edm.Double | Yes | Taxable Amount Previous Year | Importe imponible del año anterior |
| 13 | `WTaxAmountPreviousYear` | Edm.Double | Yes | W Tax Amount Previous Year | Importe de retención del año anterior |
| 14 | `ExpensesReimbursed` | Edm.Double | Yes | Expenses Reimbursed | Gastos reembolsados |
| 15 | `WTaxReimbursed` | Edm.Double | Yes | W Tax Reimbursed | Retención reembolsada |
| 16 | `ReturnedAmountAfterDeductionOfWTax` | Edm.Double | Yes | Returned Amount After Deduction Of W Tax | Importe devuelto tras deducir retención |
| 17 | `DeliveryIdentificationNo` | Edm.String | Yes | Delivery Identification Number | Número de identificación de entrega |
| 18 | `SingleCertificationNo` | Edm.String | Yes | Single Certification Number | N.º de certificación único |
| 19 | `EarningYear` | Edm.Int32 | Yes | Earning Year | Año de ingresos |
| 20 | `Advanced` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Advanced | Avanzado |
| 21 | `WTaxTypeCode` | Edm.String | Yes | W Tax Type Code | Código de tipo de retención |
| 22 | `SocialSecurityFiscalC` | Edm.String | Yes | Social Security Fiscal C | Código fiscal de seguridad social |
| 23 | `SocialSecurityInstitut` | Edm.String | Yes | Social Security Institut | Institución de seguridad social |
| 24 | `CompanyCode` | Edm.String | Yes | Company Code | Código de la sociedad |
| 25 | `Category` | [BoOSWACategoryEnum](../Enums/BoOSWACategoryEnum.md) | Yes | Category | Categoría |
| 26 | `EmployeeSocialSecurity` | Edm.Double | Yes | Employee Social Security | Seguridad social del empleado |
| 27 | `EmployerSocialSecurity` | Edm.Double | Yes | Employer Social Security | Seguridad social del empleador |
| 28 | `OtherContributions` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Other Contributions | Otras contribuciones |
| 29 | `ValueOfOtherContribut` | Edm.Double | Yes | Value Of Other Contribut | Valor de otras contribuciones |
| 30 | `OtherAmountsDue` | Edm.Double | Yes | Other Amounts Due | Otros importes adeudados |
| 31 | `OtherAmountsPaid` | Edm.Double | Yes | Other Amounts Paid | Otros importes pagados |
| 32 | `AmountPaidBeforeBankr` | Edm.Double | Yes | Amount Paid Before Bankr | Importe pagado antes de la quiebra |
| 33 | `AmountPaidByTrustee` | Edm.Double | Yes | Amount Paid By Trustee | Importe pagado por el síndico |
| 34 | `FiscalCode` | Edm.String | Yes | Fiscal Code | Código fiscal |
| 35 | `TaxableAmount` | Edm.Double | Yes | Taxable Amount | Importe imponible |
| 36 | `TaxAmount` | Edm.Double | Yes | Tax Amount | Importe de impuestos |
| 37 | `TaxAmountInAdvance` | Edm.Double | Yes | Tax Amount In Advance | Importe de impuestos por adelantado |
| 38 | `SuspendedWTHTax` | Edm.Double | Yes | Suspended WTH Tax | Retención suspendida |
| 39 | `AdditionalRegionalTax57` | Edm.Double | Yes | Additional Regional Tax 57 | Impuesto regional adicional 57 |
| 40 | `AdditionalRegionalTax58` | Edm.Double | Yes | Additional Regional Tax 58 | Impuesto regional adicional 58 |
| 41 | `SuspendedRegionalTax` | Edm.Double | Yes | Suspended Regional Tax | Impuesto regional suspendido |
| 42 | `AdditionalCitytaxToI60` | Edm.Double | Yes | Additional Citytax To I 60 | Impuesto municipal adicional (I60) |
| 43 | `AdditionalCityTaxToI` | Edm.Double | Yes | Additional City Tax To I | Impuesto municipal adicional (I) |
| 44 | `SuspendedCityTax` | Edm.Double | Yes | Suspended City Tax | Impuesto municipal suspendido |
| 45 | `FiscalCodeThirdParty71` | Edm.String | Yes | Fiscal Code Third Party 71 | Código fiscal de tercero (71) |
| 46 | `FiscalCodeThirdParty72` | Edm.String | Yes | Fiscal Code Third Party 72 | Código fiscal de tercero (72) |
| 47 | `FiscalCodeExpropriation` | Edm.String | Yes | Fiscal Code Expropriation | Código fiscal de expropiación |
| 48 | `FiscalCodeOfMainDeb101` | Edm.String | Yes | Fiscal Code Of Main Deb 101 | Código fiscal del deudor principal (101) |
| 49 | `AmountPaid102` | Edm.Double | Yes | Amount Paid 102 | Importe pagado (casilla 102) |
| 50 | `AmountsProvidedAndNo104` | Edm.Double | Yes | Amounts Provided And Number 104 | Importes provistos y N.º (casilla 104) |
| 51 | `WHTApplied103` | Edm.Double | Yes | WHT Applied 103 | Retención aplicada (casilla 103) |
| 52 | `FiscalCodeOfMainDeb105` | Edm.String | Yes | Fiscal Code Of Main Deb 105 | Código fiscal del deudor principal (105) |
| 53 | `AmountPaid106` | Edm.Double | Yes | Amount Paid 106 | Importe pagado (casilla 106) |
| 54 | `AmountsProvidedAndNo108` | Edm.Double | Yes | Amounts Provided And Number 108 | Importes provistos y N.º (casilla 108) |
| 55 | `WHTApplied107` | Edm.Double | Yes | WHT Applied 107 | Retención aplicada (casilla 107) |
| 56 | `AmountPaid131` | Edm.Double | Yes | Amount Paid 131 | Importe pagado (casilla 131) |
| 57 | `TaxApplied132` | Edm.Double | Yes | Tax Applied 132 | Impuesto aplicado (casilla 132) |
| 58 | `AmountPaid133` | Edm.Double | Yes | Amount Paid 133 | Importe pagado (casilla 133) |
| 59 | `TaxApplied134` | Edm.Double | Yes | Tax Applied 134 | Impuesto aplicado (casilla 134) |
| 60 | `AmountPaid135` | Edm.Double | Yes | Amount Paid 135 | Importe pagado (casilla 135) |
| 61 | `TaxApplied136` | Edm.Double | Yes | Tax Applied 136 | Impuesto aplicado (casilla 136) |
| 62 | `AmountPaid137` | Edm.Double | Yes | Amount Paid 137 | Importe pagado (casilla 137) |
| 63 | `TaxApplied138` | Edm.Double | Yes | Tax Applied 138 | Impuesto aplicado (casilla 138) |

## Navigation properties (3)

Use `GET /b1s/v2/SpecificWTHAmountsService(PaymentReasonCode='value',CardCode='value',CUSplit='value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `PaymentReasonCode2` | [PaymentReasonCode](../Entidades/PaymentReasonCodes.md) | [PaymentReasonCodes](PaymentReasonCodes.md) | PaymentReasonCode → Code | Códigos de motivo de pago |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CardCode → CardCode | Socio de negocios |
| `WTaxTypeCode2` | [WTaxTypeCode](../Entidades/WTaxTypeCodes.md) | [WTaxTypeCodes](WTaxTypeCodes.md) | WTaxTypeCode → Code | Códigos de tipo de retención |
