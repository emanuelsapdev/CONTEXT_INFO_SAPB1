# WithholdingTaxCodes — Códigos de retención de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WithholdingTaxCodes`
- **Descripción (ES):** Códigos de retención de impuestos
- **Entity type:** `WithholdingTaxCode` (open type: accepts dynamic/UDF properties)
- **Key:** `WTCode` (Edm.String)
- **DB tables (main / lines):** [OWHT](../../Tablas%20SAP%20B1/OWHT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 58 · **Navigation properties:** 11 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WithholdingTaxCodes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WithholdingTaxCodes/$count` | Contar |
| Get by key | `GET /b1s/v2/WithholdingTaxCodes('value')` | Obtener por clave |
| Create | `POST /b1s/v2/WithholdingTaxCodes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WithholdingTaxCodes('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WithholdingTaxCodes('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/WithholdingTaxCodes('value')` (only if the B1 object allows removal) | Borrar |

## Properties (58)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `WTCode` 🔑 | Edm.String | No | Withholding Tax Code | Código de retención |
| 2 | `WTName` | Edm.String | Yes | Withholding Tax Name | Nombre de la retención |
| 3 | `Category` | [WithholdingTaxCodeCategoryEnum](../Enums/WithholdingTaxCodeCategoryEnum.md) | Yes | Category | Categoría |
| 4 | `BaseType` | [WithholdingTaxCodeBaseTypeEnum](../Enums/WithholdingTaxCodeBaseTypeEnum.md) | Yes | Base Type | Tipo base (tipo de objeto del documento base) |
| 5 | `BaseAmount` | Edm.Double | Yes | Base Amount | Importe base |
| 6 | `OfficialCode` | Edm.String | Yes | Official Code | Código oficial |
| 7 | `Account` | Edm.String | Yes | Account | Cuenta |
| 8 | `WithholdingType` | [WithholdingTypeEnum](../Enums/WithholdingTypeEnum.md) | Yes | Withholding Type | Tipo de retención |
| 9 | `RoundingType` | [RoundingTypeEnum](../Enums/RoundingTypeEnum.md) | Yes | Rounding Type | Tipo de redondeo |
| 10 | `Section` | Edm.Int32 | Yes | Section | Sección |
| 11 | `Threshold` | Edm.Double | Yes | Threshold | Umbral |
| 12 | `Surcharge` | Edm.Double | Yes | Surcharge | Recargo |
| 13 | `Concessional` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Concessional | Concesional |
| 14 | `Assessee` | Edm.Int32 | Yes | Assessee | Contribuyente |
| 15 | `APTDSAccount` | Edm.String | Yes | APTDS Account | Cuenta TDS (compras) |
| 16 | `APSurchargeAccount` | Edm.String | Yes | AP Surcharge Account | Cuenta de recargo (compras) |
| 17 | `APCessAccount` | Edm.String | Yes | AP Cess Account | Cuenta de Cess (compras) |
| 18 | `APHSCAccount` | Edm.String | Yes | APHSC Account | Cuenta HSC (compras) |
| 19 | `APIGSTAccount` | Edm.String | Yes | APIGST Account | Cuenta IGST (compras) |
| 20 | `APCGSTAccount` | Edm.String | Yes | APCGST Account | Cuenta CGST (compras) |
| 21 | `APSGSTAccount` | Edm.String | Yes | APSGST Account | Cuenta SGST (compras) |
| 22 | `APUTGSTAccount` | Edm.String | Yes | APUTGST Account | Cuenta UTGST (compras) |
| 23 | `APCessGSTAccount` | Edm.String | Yes | AP Cess GST Account | Cuenta de Cess GST (compras) |
| 24 | `ARTDSAccount` | Edm.String | Yes | ARTDS Account | Cuenta TDS (ventas) |
| 25 | `ARSurchargeAccount` | Edm.String | Yes | AR Surcharge Account | Cuenta de recargo (ventas) |
| 26 | `ARCessAccount` | Edm.String | Yes | AR Cess Account | Cuenta de Cess (ventas) |
| 27 | `ARHSCAccount` | Edm.String | Yes | ARHSC Account | Cuenta HSC (ventas) |
| 28 | `ARIGSTAccount` | Edm.String | Yes | ARIGST Account | Cuenta IGST (ventas) |
| 29 | `ARCGSTAccount` | Edm.String | Yes | ARCGST Account | Cuenta CGST (ventas) |
| 30 | `ARSGSTAccount` | Edm.String | Yes | ARSGST Account | Cuenta SGST (ventas) |
| 31 | `ARUTGSTAccount` | Edm.String | Yes | ARUTGST Account | Cuenta UTGST (ventas) |
| 32 | `ARCessGSTAccount` | Edm.String | Yes | AR Cess GST Account | Cuenta de Cess GST (ventas) |
| 33 | `ARTCSInterimAccount` | Edm.String | Yes | ARTCS Interim Account | Cuenta transitoria TCS (ventas) |
| 34 | `ARSurchargeInterimAccount` | Edm.String | Yes | AR Surcharge Interim Account | Cuenta transitoria de recargo (ventas) |
| 35 | `ARCessInterimAccount` | Edm.String | Yes | AR Cess Interim Account | Cuenta transitoria de Cess (ventas) |
| 36 | `ARHSCInterimAccount` | Edm.String | Yes | ARHSC Interim Account | Cuenta transitoria HSC (ventas) |
| 37 | `APTCSInterimAccount` | Edm.String | Yes | APTCS Interim Account | Cuenta transitoria TCS (compras) |
| 38 | `APSurchargeInterimAccount` | Edm.String | Yes | AP Surcharge Interim Account | Cuenta transitoria de recargo (compras) |
| 39 | `APCessInterimAccount` | Edm.String | Yes | AP Cess Interim Account | Cuenta transitoria de Cess (compras) |
| 40 | `APHSCInterimAccount` | Edm.String | Yes | APHSC Interim Account | Cuenta transitoria HSC (compras) |
| 41 | `Location` | Edm.Int32 | Yes | Location | Ubicación |
| 42 | `ReturnType` | [ReturnTypeEnum](../Enums/ReturnTypeEnum.md) | Yes | Return Type | Tipo de devolución |
| 43 | `Inactive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inactive | Inactivo |
| 44 | `CSTCodeIncomingID` | Edm.Int32 | Yes | CST Code Incoming ID | ID de código CST de entrada |
| 45 | `CSTCodeOutgoingID` | Edm.Int32 | Yes | CST Code Outgoing ID | ID de código CST de salida |
| 46 | `NatureOfCalculationBaseCode` | Edm.String | Yes | Nature Of Calculation Base Code | Código de naturaleza de la base de cálculo |
| 47 | `TypeID` | Edm.Int32 | Yes | Type ID | ID de tipo |
| 48 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |
| 49 | `EffectiveFrom` | Edm.DateTimeOffset | Yes | Effective From | Vigente desde |
| 50 | `MinimumTaxableAmount` | Edm.Double | Yes | Minimum Taxable Amount | Importe imponible mínimo |
| 51 | `IsProgressiveTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Progressive Tax | Es impuesto progresivo |
| 52 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 53 | `TdsType` | [TdsTypeEnum](../Enums/TdsTypeEnum.md) | Yes | Tds Type | Tipo TDS |
| 54 | `TransactonThreshold` | Edm.Double | Yes | Transacton Threshold | Umbral de transacción |
| 55 | `EBooksWTaxCategory` | Edm.Int32 | Yes | E Books W Tax Category | Categoría de retención (libros electrónicos) |
| 56 | `NonDeductThreshold` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Non Deduct Threshold | Umbral no deducible |
| 57 | `UseInAPDPR` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use In APDPR | Usar en solicitud de anticipo de compras |
| 58 | `WithholdingTaxCodes_Lines` | Collection([WithholdingTaxCodes_Line](../Tipos-Complejos/WithholdingTaxCodes_Line.md)) | Yes | Withholding Tax Codes Lines | Líneas de códigos de retención |

## Navigation properties (11)

Use `GET /b1s/v2/WithholdingTaxCodes('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `VendorPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [VendorPayments](VendorPayments.md) |  | Pagos efectuados |
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | Account → Code | Plan de cuentas (cuentas de mayor) |
| `Section2` | [Section](../Entidades/Sections.md) | [Sections](Sections.md) | Section → AbsEntry | Secciones |
| `NatureOfAssessee` | [NatureOfAssessee](../Entidades/NatureOfAssessees.md) | [NatureOfAssessees](NatureOfAssessees.md) | Assessee → AbsEntry | Naturaleza de contribuyentes |
| `WarehouseLocation` | [WarehouseLocation](../Entidades/WarehouseLocations.md) | [WarehouseLocations](WarehouseLocations.md) | Location → Code | Ubicaciones de almacenes |
| `NotaFiscalCST` | [NotaFiscalCST](../Entidades/NotaFiscalCST.md) | [NotaFiscalCST](NotaFiscalCST.md) | CSTCodeIncomingID → ID | CST de Nota Fiscal |
| `BrazilStringIndexer` | [BrazilStringIndexer](../Entidades/BrazilStringIndexers.md) | [BrazilStringIndexers](BrazilStringIndexers.md) | NatureOfCalculationBaseCode → ID | Brasil - Indexadores de cadenas |
| `Currency2` | [Currency](../Entidades/Currencies.md) | [Currencies](Currencies.md) | Currency → Code | Monedas |
| `PaymentDrafts` | Collection([Payment](../Entidades/VendorPayments.md)) | [PaymentDrafts](PaymentDrafts.md) |  | Borradores de pagos |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
| `IncomingPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [IncomingPayments](IncomingPayments.md) |  | Pagos recibidos |
