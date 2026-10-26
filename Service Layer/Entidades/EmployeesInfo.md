# EmployeesInfo — Empleados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `EmployeesInfo`
- **Descripción (ES):** Empleados
- **Entity type:** `EmployeeInfo` (open type: accepts dynamic/UDF properties)
- **Key:** `EmployeeID` (Edm.Int32)
- **DB tables (main / lines):** [OHEM](../../Tablas%20SAP%20B1/OHEM.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 125 · **Navigation properties:** 53 · **Bound actions:** 2

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/EmployeesInfo?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/EmployeesInfo/$count` | Contar |
| Get by key | `GET /b1s/v2/EmployeesInfo(1)` | Obtener por clave |
| Create | `POST /b1s/v2/EmployeesInfo` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/EmployeesInfo(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/EmployeesInfo(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/EmployeesInfo(1)` (only if the B1 object allows removal) | Borrar |
| Action `Cancel` | `POST /b1s/v2/EmployeesInfo(1)/Cancel` | Cancelar |
| Action `Close` | `POST /b1s/v2/EmployeesInfo(1)/Close` | Cerrar |

## Properties (125)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `EmployeeID` 🔑 | Edm.Int32 | No | Employee ID | ID de empleado |
| 2 | `LastName` | Edm.String | Yes | Last Name | Apellido |
| 3 | `FirstName` | Edm.String | Yes | First Name | Nombre |
| 4 | `MiddleName` | Edm.String | Yes | Middle Name | Segundo nombre |
| 5 | `Gender` | [BoGenderTypes](../Enums/BoGenderTypes.md) | Yes | Gender | Sexo |
| 6 | `JobTitle` | Edm.String | Yes | Job Title | Cargo |
| 7 | `EmployeeType` | Edm.Int32 | Yes | Employee Type | Tipo de empleado |
| 8 | `Department` | Edm.Int32 | Yes | Department | Departamento |
| 9 | `Branch` | Edm.Int32 | Yes | Branch | Sucursal |
| 10 | `WorkStreet` | Edm.String | Yes | Work Street | Calle (trabajo) |
| 11 | `WorkBlock` | Edm.String | Yes | Work Block | Barrio (trabajo) |
| 12 | `WorkZipCode` | Edm.String | Yes | Work Zip Code | Código postal (trabajo) |
| 13 | `WorkCity` | Edm.String | Yes | Work City | Ciudad (trabajo) |
| 14 | `WorkCounty` | Edm.String | Yes | Work County | Condado (trabajo) |
| 15 | `WorkCountryCode` | Edm.String | Yes | Work Country Code | País (trabajo) |
| 16 | `WorkStateCode` | Edm.String | Yes | Work State Code | Estado (trabajo) |
| 17 | `Manager` | Edm.Int32 | Yes | Manager | Responsable |
| 18 | `ApplicationUserID` | Edm.Int32 | Yes | Application User ID | ID de usuario de la aplicación |
| 19 | `SalesPersonCode` | Edm.Int32 | Yes | Sales Person Code | Código del empleado de ventas |
| 20 | `OfficePhone` | Edm.String | Yes | Office Phone | Teléfono de oficina |
| 21 | `OfficeExtension` | Edm.String | Yes | Office Extension | Interno (extensión) |
| 22 | `MobilePhone` | Edm.String | Yes | Mobile Phone | Teléfono celular |
| 23 | `Pager` | Edm.String | Yes | Pager | Buscapersonas |
| 24 | `HomePhone` | Edm.String | Yes | Home Phone | Teléfono particular |
| 25 | `Fax` | Edm.String | Yes | Fax | Fax |
| 26 | `eMail` | Edm.String | Yes | E Mail | Correo electrónico |
| 27 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 28 | `StatusCode` | Edm.Int32 | Yes | Status Code | Código de estado |
| 29 | `Salary` | Edm.Double | Yes | Salary | Salario |
| 30 | `SalaryUnit` | [BoSalaryCostUnits](../Enums/BoSalaryCostUnits.md) | Yes | Salary Unit | Unidad del salario |
| 31 | `EmployeeCosts` | Edm.Double | Yes | Employee Costs | Costos del empleado |
| 32 | `EmployeeCostUnit` | [BoSalaryCostUnits](../Enums/BoSalaryCostUnits.md) | Yes | Employee Cost Unit | Unidad de costo del empleado |
| 33 | `TerminationDate` | Edm.DateTimeOffset | Yes | Termination Date | Fecha de terminación |
| 34 | `TreminationReason` | Edm.Int32 | Yes | Tremination Reason | Motivo de baja |
| 35 | `BankCode` | Edm.String | Yes | Bank Code | Código del banco |
| 36 | `BankBranch` | Edm.String | Yes | Bank Branch | Sucursal bancaria |
| 37 | `BankBranchNum` | Edm.String | Yes | Bank Branch Number | Número de sucursal bancaria |
| 38 | `BankAccount` | Edm.String | Yes | Bank Account | Cuenta bancaria |
| 39 | `HomeStreet` | Edm.String | Yes | Home Street | Calle (domicilio) |
| 40 | `HomeBlock` | Edm.String | Yes | Home Block | Barrio (domicilio) |
| 41 | `HomeZipCode` | Edm.String | Yes | Home Zip Code | Código postal (domicilio) |
| 42 | `HomeCity` | Edm.String | Yes | Home City | Ciudad (domicilio) |
| 43 | `HomeCounty` | Edm.String | Yes | Home County | Condado (domicilio) |
| 44 | `HomeCountry` | Edm.String | Yes | Home Country | País (domicilio) |
| 45 | `HomeState` | Edm.String | Yes | Home State | Estado/provincia (domicilio) |
| 46 | `DateOfBirth` | Edm.DateTimeOffset | Yes | Date Of Birth | Fecha de nacimiento |
| 47 | `CountryOfBirth` | Edm.String | Yes | Country Of Birth | País de nacimiento |
| 48 | `MartialStatus` | [BoMeritalStatuses](../Enums/BoMeritalStatuses.md) | Yes | Martial Status | Estado civil |
| 49 | `NumOfChildren` | Edm.Int32 | Yes | Number Of Children | Cantidad de hijos |
| 50 | `IdNumber` | Edm.String | Yes | ID Number | Número de identificación |
| 51 | `CitizenshipCountryCode` | Edm.String | Yes | Citizenship Country Code | Código de país de ciudadanía |
| 52 | `PassportNumber` | Edm.String | Yes | Passport Number | Número de pasaporte |
| 53 | `PassportExpirationDate` | Edm.DateTimeOffset | Yes | Passport Expiration Date | Fecha de vencimiento del pasaporte |
| 54 | `Picture` | Edm.String | Yes | Picture | Imagen |
| 55 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 56 | `SalaryCurrency` | Edm.String | Yes | Salary Currency | Moneda del salario |
| 57 | `EmployeeCostsCurrency` | Edm.String | Yes | Employee Costs Currency | Moneda de costos del empleado |
| 58 | `WorkBuildingFloorRoom` | Edm.String | Yes | Work Building Floor Room | Edificio/piso (trabajo) |
| 59 | `HomeBuildingFloorRoom` | Edm.String | Yes | Home Building Floor Room | Edificio/piso (domicilio) |
| 60 | `Position` | Edm.Int32 | Yes | Position | Posición/cargo |
| 61 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 62 | `CostCenterCode` | Edm.String | Yes | Cost Center Code | Código de centro de costo |
| 63 | `CompanyNumber` | Edm.String | Yes | Company Number | Número de la sociedad |
| 64 | `VacationPreviousYear` | Edm.Int32 | Yes | Vacation Previous Year | Vacaciones del año anterior |
| 65 | `VacationCurrentYear` | Edm.Int32 | Yes | Vacation Current Year | Vacaciones del año actual |
| 66 | `MunicipalityKey` | Edm.String | Yes | Municipality Key | Clave del municipio |
| 67 | `TaxClass` | Edm.String | Yes | Tax Class | Clase de impuesto |
| 68 | `IncomeTaxLiability` | Edm.String | Yes | Income Tax Liability | Obligación del impuesto a las ganancias |
| 69 | `Religion` | Edm.String | Yes | Religion | Religión |
| 70 | `PartnerReligion` | Edm.String | Yes | Partner Religion | Religión del cónyuge |
| 71 | `ExemptionAmount` | Edm.Double | Yes | Exemption Amount | Importe de exención |
| 72 | `ExemptionUnit` | [EmployeeExemptionUnitEnum](../Enums/EmployeeExemptionUnitEnum.md) | Yes | Exemption Unit | Unidad de exención |
| 73 | `ExemptionCurrency` | Edm.String | Yes | Exemption Currency | Moneda de exención |
| 74 | `AdditionalAmount` | Edm.Double | Yes | Additional Amount | Importe adicional |
| 75 | `AdditionalUnit` | [EmployeeExemptionUnitEnum](../Enums/EmployeeExemptionUnitEnum.md) | Yes | Additional Unit | Unidad adicional |
| 76 | `AdditionalCurrency` | Edm.String | Yes | Additional Currency | Moneda adicional |
| 77 | `TaxOfficeName` | Edm.String | Yes | Tax Office Name | Nombre de la oficina tributaria |
| 78 | `TaxOfficeNumber` | Edm.String | Yes | Tax Office Number | Número de oficina tributaria |
| 79 | `HealthInsuranceName` | Edm.String | Yes | Health Insurance Name | Nombre del seguro de salud |
| 80 | `HealthInsuranceCode` | Edm.String | Yes | Health Insurance Code | Código de seguro de salud |
| 81 | `HealthInsuranceType` | Edm.String | Yes | Health Insurance Type | Tipo de seguro de salud |
| 82 | `SocialInsuranceNumber` | Edm.String | Yes | Social Insurance Number | Número de seguro social |
| 83 | `ProfessionStatus` | Edm.String | Yes | Profession Status | Situación profesional |
| 84 | `EducationStatus` | Edm.String | Yes | Education Status | Estado de formación |
| 85 | `PersonGroup` | Edm.String | Yes | Person Group | Grupo de personas |
| 86 | `JobTitleCode` | Edm.String | Yes | Job Title Code | Código de cargo |
| 87 | `BankCodeForDATEV` | Edm.String | Yes | Bank Code For DATEV | Código bancario para DATEV |
| 88 | `DeviatingBankAccountOwner` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Deviating Bank Account Owner | Titular alternativo de la cuenta bancaria |
| 89 | `SpouseFirstName` | Edm.String | Yes | Spouse First Name | Nombre del cónyuge |
| 90 | `SpouseSurname` | Edm.String | Yes | Spouse Surname | Apellido del cónyuge |
| 91 | `ExternalEmployeeNumber` | Edm.String | Yes | External Employee Number | Número de empleado externo |
| 92 | `BirthPlace` | Edm.String | Yes | Birth Place | Lugar de nacimiento |
| 93 | `PaymentMethod` | [EmployeePaymentMethodEnum](../Enums/EmployeePaymentMethodEnum.md) | Yes | Payment Method | Vía de pago |
| 94 | `STDCode` | Edm.Int32 | Yes | STD Code | Código STD |
| 95 | `CPF` | Edm.String | Yes | CPF | CPF (Brasil) |
| 96 | `CRCNumber` | Edm.String | Yes | CRC Number | Número CRC |
| 97 | `AccountantResponsible` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Accountant Responsible | Contador responsable |
| 98 | `LegalRepresentative` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Legal Representative | Representante legal |
| 99 | `DIRFResponsible` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | DIRF Responsible | Responsable DIRF (Brasil) |
| 100 | `CRCState` | Edm.String | Yes | CRC State | Estado CRC |
| 101 | `Active` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active | Activo |
| 102 | `IDType` | Edm.String | Yes | ID Type | Tipo de identificación |
| 103 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |
| 104 | `PassportIssueDate` | Edm.DateTimeOffset | Yes | Passport Issue Date | Fecha de emisión del pasaporte |
| 105 | `PassportIssuer` | Edm.String | Yes | Passport Issuer | Emisor del pasaporte |
| 106 | `QualificationCode` | [SPEDContabilQualificationCodeEnum](../Enums/SPEDContabilQualificationCodeEnum.md) | Yes | Qualification Code | Código de calificación |
| 107 | `PRWebAccess` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | PR Web Access | Acceso web PR |
| 108 | `PreviousPRWebAccess` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Previous PR Web Access | Acceso web PR anterior |
| 109 | `WorkStreetNumber` | Edm.String | Yes | Work Street Number | Número de calle (trabajo) |
| 110 | `HomeStreetNumber` | Edm.String | Yes | Home Street Number | Número de calle (domicilio) |
| 111 | `LinkedVendor` | Edm.String | Yes | Linked Vendor | Proveedor vinculado |
| 112 | `CreateDate` | Edm.DateTimeOffset | Yes | Create Date | Fecha de creación |
| 113 | `CreateTime` | Edm.TimeOfDay | Yes | Create Time | Hora de creación |
| 114 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 115 | `UpdateTime` | Edm.TimeOfDay | Yes | Update Time | Hora de actualización |
| 116 | `EmployeeCode` | Edm.String | Yes | Employee Code | Código de empleado |
| 117 | `ARetSEFAZ` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | A Ret SEFAZ | Retorno SEFAZ |
| 118 | `GenderEx` | Edm.String | Yes | Gender Ex | Sexo (ampliado) |
| 119 | `EmployeeAbsenceInfoLines` | Collection([EmployeeAbsenceInfo](../Tipos-Complejos/EmployeeAbsenceInfo.md)) | Yes | Employee Absence Information Lines | Líneas de ausencias del empleado |
| 120 | `EmployeeEducationInfoLines` | Collection([EmployeeEducationInfo](../Tipos-Complejos/EmployeeEducationInfo.md)) | Yes | Employee Education Information Lines | Líneas de formación del empleado |
| 121 | `EmployeeReviewsInfoLines` | Collection([EmployeeReviewsInfo](../Tipos-Complejos/EmployeeReviewsInfo.md)) | Yes | Employee Reviews Information Lines | Líneas de evaluaciones del empleado |
| 122 | `EmployeePreviousEmpoymentInfoLines` | Collection([EmployeePreviousEmpoymentInfo](../Tipos-Complejos/EmployeePreviousEmpoymentInfo.md)) | Yes | Employee Previous Empoyment Information Lines | Líneas de empleos anteriores |
| 123 | `EmployeeRolesInfoLines` | Collection([EmployeeRolesInfo](../Tipos-Complejos/EmployeeRolesInfo.md)) | Yes | Employee Roles Information Lines | Líneas de funciones del empleado |
| 124 | `EmployeeSavingsPaymentInfoLines` | Collection([EmployeeSavingsPaymentInfo](../Tipos-Complejos/EmployeeSavingsPaymentInfo.md)) | Yes | Employee Savings Payment Information Lines | Líneas de pagos de ahorro del empleado |
| 125 | `EmployeeBranchAssignment` | Collection([EmployeeBranchAssignmentItem](../Tipos-Complejos/EmployeeBranchAssignmentItem.md)) | Yes | Employee Branch Assignment | Asignación de sucursales del empleado |

## Navigation properties (53)

Use `GET /b1s/v2/EmployeesInfo(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `SalesOpportunities` | Collection([SalesOpportunities](../Entidades/SalesOpportunities.md)) | [SalesOpportunities](SalesOpportunities.md) |  | Oportunidades de venta |
| `Warehouses` | Collection([Warehouse](../Entidades/Warehouses.md)) | [Warehouses](Warehouses.md) |  | Almacenes |
| `ProfitCenters` | Collection([ProfitCenter](../Entidades/ProfitCenters.md)) | [ProfitCenters](ProfitCenters.md) |  | Centros de beneficio/costo |
| `PurchaseQuotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseQuotations](PurchaseQuotations.md) |  | Ofertas de compra |
| `CorrectionInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoiceReversal](CorrectionInvoiceReversal.md) |  | Anulación de factura de corrección de clientes |
| `CustomerEquipmentCards` | Collection([CustomerEquipmentCard](../Entidades/CustomerEquipmentCards.md)) | [CustomerEquipmentCards](CustomerEquipmentCards.md) |  | Tarjetas de equipo del cliente |
| `CorrectionInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoice](CorrectionInvoice.md) |  | Factura de corrección de clientes |
| `PurchaseDeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDeliveryNotes](PurchaseDeliveryNotes.md) |  | Pedidos de entrada de mercancías |
| `CorrectionPurchaseInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoice](CorrectionPurchaseInvoice.md) |  | Factura de corrección de proveedores |
| `InventoryGenEntries` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenEntries](InventoryGenEntries.md) |  | Entradas de mercancías |
| `ServiceCalls` | Collection([ServiceCall](../Entidades/ServiceCalls.md)) | [ServiceCalls](ServiceCalls.md) |  | Llamadas de servicio |
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `EmployeeRoleSetup` | [EmployeeRoleSetup](../Entidades/EmployeeRolesSetup.md) | [EmployeeRolesSetup](EmployeeRolesSetup.md) | EmployeeType → TypeID | Funciones de empleados |
| `Department2` | [Department](../Entidades/Departments.md) | [Departments](Departments.md) | Department → Code | Departamentos |
| `Branch2` | [Branch](../Entidades/Branches.md) | [Branches](Branches.md) | Branch → Code | Sucursales |
| `Country` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | WorkCountryCode → Code | País |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | ApplicationUserID → InternalKey | Usuario |
| `SalesPerson` | [SalesPerson](../Entidades/SalesPersons.md) | [SalesPersons](SalesPersons.md) | SalesPersonCode → SalesEmployeeCode | Empleado de ventas |
| `EmployeeStatus` | [EmployeeStatus](../Entidades/EmployeeStatus.md) | [EmployeeStatus](EmployeeStatus.md) | StatusCode → StatusId | Estados de empleados |
| `TerminationReason` | [TerminationReason](../Entidades/TerminationReason.md) | [TerminationReason](TerminationReason.md) | TreminationReason → ReasonID | Motivos de baja |
| `Bank` | [Bank](../Entidades/Banks.md) | [Banks](Banks.md) | BankCode → AbsoluteEntry | Banco |
| `EmployeePosition` | [EmployeePosition](../Entidades/EmployeePosition.md) | [EmployeePosition](EmployeePosition.md) | Position → PositionID | Puestos de empleados |
| `ProfitCenter` | [ProfitCenter](../Entidades/ProfitCenters.md) | [ProfitCenters](ProfitCenters.md) | CostCenterCode → CenterCode | Centro de beneficio |
| `EmployeeIDType` | [EmployeeIDType](../Entidades/EmployeeIDType.md) | [EmployeeIDType](EmployeeIDType.md) | IDType → IDType | Tipos de identificación de empleado |
| `BusinessPlace` | [BusinessPlace](../Entidades/BusinessPlaces.md) | [BusinessPlaces](BusinessPlaces.md) | BPLID → BPLID | Lugar de negocios |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | LinkedVendor → CardCode | Socio de negocios |
| `Gender2` | [Gender](../Entidades/Genders.md) | [Genders](Genders.md) | GenderEx → Code | Sexos |
| `Orders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Orders](Orders.md) |  | Pedidos de cliente (órdenes de venta) |
| `InventoryGenExits` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenExits](InventoryGenExits.md) |  | Salidas de mercancías |
| `Drafts` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Drafts](Drafts.md) |  | Borradores de documentos |
| `ReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [ReturnRequest](ReturnRequest.md) |  | Solicitudes de devolución de clientes |
| `DeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DeliveryNotes](DeliveryNotes.md) |  | Entregas |
| `PurchaseInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseInvoices](PurchaseInvoices.md) |  | Facturas de proveedores |
| `SelfInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfInvoices](SelfInvoices.md) |  | Autofacturas |
| `BlanketAgreements` | Collection([BlanketAgreement](../Entidades/BlanketAgreements.md)) | [BlanketAgreements](BlanketAgreements.md) |  | Acuerdos globales |
| `Invoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Invoices](Invoices.md) |  | Facturas de clientes |
| `Campaigns` | Collection([Campaign](../Entidades/Campaigns.md)) | [Campaigns](Campaigns.md) |  | Campañas |
| `CreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CreditNotes](CreditNotes.md) |  | Notas de crédito de clientes |
| `PurchaseCreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseCreditNotes](PurchaseCreditNotes.md) |  | Notas de crédito de proveedores |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
| `DownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DownPayments](DownPayments.md) |  | Facturas de anticipo de clientes |
| `PurchaseDownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDownPayments](PurchaseDownPayments.md) |  | Facturas de anticipo de proveedores |
| `ProjectManagementTimeSheet` | Collection([PM_TimeSheetData](../Entidades/ProjectManagementTimeSheet.md)) | [ProjectManagementTimeSheet](ProjectManagementTimeSheet.md) |  | Hojas de horas de gestión de proyectos |
| `PurchaseReturns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseReturns](PurchaseReturns.md) |  | Devoluciones de mercancías a proveedores |
| `Activities` | Collection([Activity](../Entidades/Activities.md)) | [Activities](Activities.md) |  | Actividades |
| `PurchaseOrders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseOrders](PurchaseOrders.md) |  | Pedidos de compra (órdenes de compra) |
| `SelfCreditMemos` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfCreditMemos](SelfCreditMemos.md) |  | Autonotas de crédito |
| `Quotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Quotations](Quotations.md) |  | Ofertas de ventas (cotizaciones) |
| `Returns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Returns](Returns.md) |  | Devoluciones de clientes |
| `ProjectManagements` | Collection([PM_ProjectDocumentData](../Entidades/ProjectManagements.md)) | [ProjectManagements](ProjectManagements.md) |  | Gestión de proyectos |
| `GoodsReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [GoodsReturnRequest](GoodsReturnRequest.md) |  | Solicitudes de devolución de mercancías |
| `CorrectionPurchaseInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoiceReversal](CorrectionPurchaseInvoiceReversal.md) |  | Anulación de factura de corrección de proveedores |
| `PurchaseRequests` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseRequests](PurchaseRequests.md) |  | Solicitudes de compra |

## Bound actions (2)

### Cancel

- **Descripción (ES):** Cancelar
- **Request:** `POST /b1s/v2/EmployeesInfo(1)/Cancel`

### Close

- **Descripción (ES):** Cerrar
- **Request:** `POST /b1s/v2/EmployeesInfo(1)/Close`

