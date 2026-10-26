# BlanketAgreements — Acuerdos globales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BlanketAgreements`
- **Descripción (ES):** Acuerdos globales
- **Entity type:** `BlanketAgreement` (open type: accepts dynamic/UDF properties)
- **Key:** `AgreementNo` (Edm.Int32)
- **DB tables (main / lines):** [OOAT](../../Tablas%20SAP%20B1/OOAT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 37 · **Navigation properties:** 14 · **Bound actions:** 2

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BlanketAgreements?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BlanketAgreements/$count` | Contar |
| Get by key | `GET /b1s/v2/BlanketAgreements(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BlanketAgreements` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BlanketAgreements(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BlanketAgreements(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BlanketAgreements(1)` (only if the B1 object allows removal) | Borrar |
| Action `CancelBlanketAgreement` | `POST /b1s/v2/BlanketAgreements(1)/CancelBlanketAgreement` | Cancelar acuerdo global |
| Action `GetRelatedDocuments` | `POST /b1s/v2/BlanketAgreements(1)/GetRelatedDocuments` | Obtener documentos relacionados |

## Properties (37)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AgreementNo` 🔑 | Edm.Int32 | No | Agreement Number | Número de acuerdo |
| 2 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 3 | `BPName` | Edm.String | Yes | Business Partner Name | Nombre del socio de negocios |
| 4 | `ContactPersonCode` | Edm.Int32 | Yes | Contact Person Code | Código de persona de contacto |
| 5 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 6 | `EndDate` | Edm.DateTimeOffset | Yes | End Date | Fecha de fin |
| 7 | `TerminateDate` | Edm.DateTimeOffset | Yes | Terminate Date | Fecha de baja |
| 8 | `Description` | Edm.String | Yes | Description | Descripción |
| 9 | `AgreementType` | [BlanketAgreementTypeEnum](../Enums/BlanketAgreementTypeEnum.md) | Yes | Agreement Type | Tipo de acuerdo |
| 10 | `Status` | [BlanketAgreementStatusEnum](../Enums/BlanketAgreementStatusEnum.md) | Yes | Status | Estado |
| 11 | `Owner` | Edm.Int32 | Yes | Owner | Titular |
| 12 | `IgnorePricesInAgreement` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Ignore Prices In Agreement | Ignorar precios del acuerdo |
| 13 | `Renewal` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Renewal | Renovación |
| 14 | `RemindUnit` | [BoRemindUnits](../Enums/BoRemindUnits.md) | Yes | Remind Unit | Unidad de recordatorio |
| 15 | `RemindTime` | Edm.Int32 | Yes | Remind Time | Hora de recordatorio |
| 16 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 17 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 18 | `SettlementProbability` | Edm.Double | Yes | Settlement Probability | Probabilidad de cierre |
| 19 | `AgreementMethod` | [BlanketAgreementMethodEnum](../Enums/BlanketAgreementMethodEnum.md) | Yes | Agreement Method | Método del acuerdo |
| 20 | `PaymentTerms` | Edm.Int32 | Yes | Payment Terms | Condiciones de pago |
| 21 | `PriceList` | Edm.Int32 | Yes | Price List | Lista de precios |
| 22 | `SigningDate` | Edm.DateTimeOffset | Yes | Signing Date | Fecha de firma |
| 23 | `AmendmentTo` | Edm.Int32 | Yes | Amendment To | Enmienda a |
| 24 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 25 | `DocNum` | Edm.Int32 | Yes | Document Number | Número de documento |
| 26 | `HandWritten` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Hand Written | Manual (numeración manual) |
| 27 | `PeriodIndicator` | Edm.String | Yes | Period Indicator | Indicador de período |
| 28 | `PaymentMethod` | Edm.String | Yes | Payment Method | Vía de pago |
| 29 | `ExchangeRate` | Edm.Double | Yes | Exchange Rate | Tipo de cambio |
| 30 | `ShippingType` | Edm.Int32 | Yes | Shipping Type | Clase de expedición |
| 31 | `NumAtCard` | Edm.String | Yes | Number At Card | Número de referencia del socio de negocios |
| 32 | `Project` | Edm.String | Yes | Project | Proyecto |
| 33 | `PriceMode` | [PriceModeEnum](../Enums/PriceModeEnum.md) | Yes | Price Mode | Modo de precio (neto/bruto) |
| 34 | `BPCurrency` | Edm.String | Yes | Business Partner Currency | Moneda del socio de negocios |
| 35 | `BPType` | [BlanketAgreementBPTypeEnum](../Enums/BlanketAgreementBPTypeEnum.md) | Yes | Business Partner Type | Tipo de socio de negocios |
| 36 | `SAPPassport` | Edm.String | Yes | SAP Passport | SAP Passport |
| 37 | `BlanketAgreements_ItemsLines` | Collection([BlanketAgreements_ItemsLine](../Tipos-Complejos/BlanketAgreements_ItemsLine.md)) | Yes | Blanket Agreements Items Lines | Líneas de artículos del acuerdo global |

## Navigation properties (14)

Use `GET /b1s/v2/BlanketAgreements(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `VendorPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [VendorPayments](VendorPayments.md) |  | Pagos efectuados |
| `JournalEntries` | Collection([JournalEntry](../Entidades/JournalEntries.md)) | [JournalEntries](JournalEntries.md) |  | Asientos contables |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | BPCode → CardCode | Socio de negocios |
| `EmployeeInfo` | [EmployeeInfo](../Entidades/EmployeesInfo.md) | [EmployeesInfo](EmployeesInfo.md) | Owner → EmployeeID | Empleados |
| `Attachments2` | [Attachments2](../Entidades/Attachments2.md) | [Attachments2](Attachments2.md) | AttachmentEntry → AbsoluteEntry | Anexos |
| `PaymentTermsType` | [PaymentTermsType](../Entidades/PaymentTermsTypes.md) | [PaymentTermsTypes](PaymentTermsTypes.md) | PaymentTerms → GroupNumber | Condiciones de pago |
| `PriceList2` | [PriceList](../Entidades/PriceLists.md) | [PriceLists](PriceLists.md) | PriceList → PriceListNo | Listas de precios |
| `WizardPaymentMethod` | [WizardPaymentMethod](../Entidades/WizardPaymentMethods.md) | [WizardPaymentMethods](WizardPaymentMethods.md) | PaymentMethod → PaymentMethodCode | Vías de pago del asistente de pagos |
| `ShippingType2` | [ShippingType](../Entidades/ShippingTypes.md) | [ShippingTypes](ShippingTypes.md) | ShippingType → Code | Clases de expedición |
| `Project2` | [Project](../Entidades/Projects.md) | [Projects](Projects.md) | Project → Code | Proyectos |
| `Currency` | [Currency](../Entidades/Currencies.md) | [Currencies](Currencies.md) | BPCurrency → Code | Moneda |
| `PaymentDrafts` | Collection([Payment](../Entidades/VendorPayments.md)) | [PaymentDrafts](PaymentDrafts.md) |  | Borradores de pagos |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
| `IncomingPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [IncomingPayments](IncomingPayments.md) |  | Pagos recibidos |

## Bound actions (2)

### CancelBlanketAgreement

- **Descripción (ES):** Cancelar acuerdo global
- **Request:** `POST /b1s/v2/BlanketAgreements(1)/CancelBlanketAgreement`

### GetRelatedDocuments

- **Descripción (ES):** Obtener documentos relacionados
- **Request:** `POST /b1s/v2/BlanketAgreements(1)/GetRelatedDocuments`
- **Returns:** Collection([BlanketAgreementsDocument](../Tipos-Complejos/BlanketAgreementsDocument.md))

