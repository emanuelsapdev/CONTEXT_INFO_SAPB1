# CompanyInfo — Información de la sociedad

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CompanyInfo`
- **Descripción (ES):** Información de la sociedad
- **Description (EN):** Company Information

- **Properties:** 36

## Properties (36)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Version` | Edm.Int32 | Yes | Version | Versión |
| 2 | `EnableExpensesManagement` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Expenses Management | Habilitar gestión de gastos |
| 3 | `EnableAccountSegmentation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Account Segmentation | Habilitar segmentación de cuentas |
| 4 | `EnableBillOfExchange` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Bill Of Exchange | Habilitar letras de cambio |
| 5 | `BaseDateForExchangeRate` | [BoBaseDateRateEnum](../Enums/BoBaseDateRateEnum.md) | Yes | Base Date For Exchange Rate | Fecha base para el tipo de cambio |
| 6 | `BISRBankActKey` | Edm.Int32 | Yes | BISR Bank Act Key | Clave de cuenta bancaria BISR |
| 7 | `BISRBankCountry` | Edm.String | Yes | BISR Bank Country | País del banco BISR |
| 8 | `BISRBankNo` | Edm.String | Yes | BISR Bank Number | Número de banco BISR |
| 9 | `BISRBankAccount` | Edm.String | Yes | BISR Bank Account | Cuenta bancaria BISR |
| 10 | `BISRBranch` | Edm.String | Yes | BISR Branch | Sucursal BISR |
| 11 | `MaxRecordsInChooseFromList` | Edm.Int32 | Yes | Max Records In Choose From List | Registros máximos en lista de selección |
| 12 | `EnableCheckQuantityInRDR` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Check Quantity In RDR | Habilitar verificación de cantidad en pedidos de cliente |
| 13 | `SRIManagementSystem` | [BoManageMethod](../Enums/BoManageMethod.md) | Yes | SRI Management System | Sistema de gestión de números de serie |
| 14 | `AutoSRICreationOnReceipt` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Auto SRI Creation On Receipt | Crear series/lotes automáticamente en la entrada |
| 15 | `IEPSPayer` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | IEPS Payer | Contribuyente de IEPS (México) |
| 16 | `DefaultDaysForOrdCanc` | Edm.Int32 | Yes | Default Days For Ord Canc | Días predeterminados para cancelación de pedidos |
| 17 | `PercentOfTotalAcquisition` | Edm.Double | Yes | Percent Of Total Acquisition | Porcentaje de la adquisición total |
| 18 | `MinimumBaseAmountPerDoc` | Edm.Double | Yes | Minimum Base Amount Per Document | Importe base mínimo por documento |
| 19 | `EnableSharingSeries` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Sharing Series | Habilitar series compartidas |
| 20 | `DataOwnershipIndication` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Data Ownership Indication | Indicación de propiedad de datos |
| 21 | `MinimumAmountForAppndixOP` | Edm.Double | Yes | Minimum Amount For Appndix OP | Importe mínimo para anexo O/P |
| 22 | `DisplayTransactionsByDflt` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Transactions By Default | Mostrar transacciones por defecto |
| 23 | `DefaultStampTax` | Edm.String | Yes | Default Stamp Tax | Impuesto de timbre predeterminado |
| 24 | `MinimumAmountForAnnualList` | Edm.Double | Yes | Minimum Amount For Annual List | Importe mínimo para lista anual |
| 25 | `BlockStockNegativeQuantity` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Stock Negative Quantity | Bloquear cantidad negativa de stock |
| 26 | `AutoCreateCustomerEqCard` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Auto Create Customer Eq Card | Crear automáticamente tarjeta de equipo del cliente |
| 27 | `MaxNumberOfDocumentsInPmt` | Edm.Int32 | Yes | Max Number Of Documents In Pmt | Cantidad máxima de documentos por pago |
| 28 | `EnableStockRelNoCostPrice` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Stock Rel Number Cost Price | Habilitar stock relevante sin precio de costo |
| 29 | `CompanyName` | Edm.String | Yes | Company Name | Nombre de la sociedad |
| 30 | `GroupLinesInVATCalculation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Group Lines In VAT Calculation | Agrupar líneas en el cálculo de IVA |
| 31 | `TaxCalculationSystem` | [TaxCalcSysEnum](../Enums/TaxCalcSysEnum.md) | Yes | Tax Calculation System | Sistema de cálculo de impuestos |
| 32 | `EnableTransactionNotification` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Transaction Notification | Habilitar Transaction Notification |
| 33 | `EnableConversionDifferentAcct` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Conversion Different Account | Habilitar cuenta de diferencias de conversión |
| 34 | `B1iTimeOut` | Edm.Int32 | Yes | B 1i Time Out | Tiempo de espera de B1i |
| 35 | `LanguageCode` | [BoSuppLangs](../Enums/BoSuppLangs.md) | Yes | Language Code | Código de idioma |
| 36 | `Localization` | Edm.String | Yes | Localization | Localización |

## Used by (service operations)

- [`CompanyService_GetCompanyInfo`](../Servicios/CompanyService.md#companyservice_getcompanyinfo)
- [`CompanyService_UpdateCompanyInfo`](../Servicios/CompanyService.md#companyservice_updatecompanyinfo)
