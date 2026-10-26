# Users — Usuarios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Users`
- **Descripción (ES):** Usuarios
- **Entity type:** `User` (open type: accepts dynamic/UDF properties)
- **Key:** `InternalKey` (Edm.Int32)
- **DB tables (main / lines):** [OUSR](../../Tablas%20SAP%20B1/OUSR.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 28 · **Navigation properties:** 51 · **Bound actions:** 2

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Users?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Users/$count` | Contar |
| Get by key | `GET /b1s/v2/Users(1)` | Obtener por clave |
| Create | `POST /b1s/v2/Users` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Users(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Users(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/Users(1)` (only if the B1 object allows removal) | Borrar |
| Action `Close` | `POST /b1s/v2/Users(1)/Close` | Cerrar |
| Action `RemoveUserAndLicense` | `POST /b1s/v2/Users(1)/RemoveUserAndLicense` | Eliminar usuario y licencia |

## Properties (28)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `InternalKey` 🔑 | Edm.Int32 | No | Internal Key | Clave interna |
| 2 | `UserPassword` | Edm.String | Yes | User Password | Contraseña del usuario |
| 3 | `UserCode` | Edm.String | Yes | User Code | Código de usuario |
| 4 | `UserName` | Edm.String | Yes | User Name | Nombre de usuario |
| 5 | `Superuser` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Superuser | Superusuario |
| 6 | `eMail` | Edm.String | Yes | E Mail | Correo electrónico |
| 7 | `MobilePhoneNumber` | Edm.String | Yes | Mobile Phone Number | Número de teléfono celular |
| 8 | `Defaults` | Edm.String | Yes | Defaults | Valores predeterminados |
| 9 | `FaxNumber` | Edm.String | Yes | Fax Number | Número de fax |
| 10 | `Branch` | Edm.Int32 | Yes | Branch | Sucursal |
| 11 | `Department` | Edm.Int32 | Yes | Department | Departamento |
| 12 | `LanguageCode` | [BoSuppLangs](../Enums/BoSuppLangs.md) | Yes | Language Code | Código de idioma |
| 13 | `Locked` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Locked | Bloqueado |
| 14 | `Group` | [BoUserGroup](../Enums/BoUserGroup.md) | Yes | Group | Grupo |
| 15 | `MaxDiscountGeneral` | Edm.Double | Yes | Max Discount General | Descuento máximo general |
| 16 | `MaxDiscountSales` | Edm.Double | Yes | Max Discount Sales | Descuento máximo de ventas |
| 17 | `MaxDiscountPurchase` | Edm.Double | Yes | Max Discount Purchase | Descuento máximo de compras |
| 18 | `CashLimit` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Cash Limit | Límite de efectivo |
| 19 | `MaxCashAmtForIncmngPayts` | Edm.Double | Yes | Max Cash Amount For Incmng Payts | Importe máximo en efectivo para pagos recibidos |
| 20 | `LastLogoutDate` | Edm.DateTimeOffset | Yes | Last Logout Date | Fecha del último cierre de sesión |
| 21 | `LastLoginTime` | Edm.TimeOfDay | Yes | Last Login Time | Hora del último inicio de sesión |
| 22 | `LastLogoutTime` | Edm.TimeOfDay | Yes | Last Logout Time | Hora del último cierre de sesión |
| 23 | `LastPasswordChangeTime` | Edm.TimeOfDay | Yes | Last Password Change Time | Hora del último cambio de contraseña |
| 24 | `LastPasswordChangedBy` | Edm.String | Yes | Last Password Changed By | Última contraseña cambiada por |
| 25 | `UserPermission` | Collection([UserPermissionItem](../Tipos-Complejos/UserPermissionItem.md)) | Yes | User Permission | Permiso del usuario |
| 26 | `UserActionRecord` | Collection([UserActionRecordItem](../Tipos-Complejos/UserActionRecordItem.md)) | Yes | User Action Record | Registro de acciones del usuario |
| 27 | `UserGroupByUser` | Collection([UserGroupByUserItem](../Tipos-Complejos/UserGroupByUserItem.md)) | Yes | User Group By User | Grupos del usuario |
| 28 | `UserBranchAssignment` | Collection([UserBranchAssignmentItem](../Tipos-Complejos/UserBranchAssignmentItem.md)) | Yes | User Branch Assignment | Asignación de sucursales del usuario |

## Navigation properties (51)

Use `GET /b1s/v2/Users(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `SalesOpportunities` | Collection([SalesOpportunities](../Entidades/SalesOpportunities.md)) | [SalesOpportunities](SalesOpportunities.md) |  | Oportunidades de venta |
| `UserDefaultGroups` | Collection([UserDefaultGroup](../Entidades/UserDefaultGroups.md)) | [UserDefaultGroups](UserDefaultGroups.md) |  | Grupos de valores predeterminados de usuario |
| `LegalData` | Collection([LegalData](../Entidades/LegalData.md)) | [LegalData](LegalData.md) |  | Datos legales |
| `PurchaseQuotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseQuotations](PurchaseQuotations.md) |  | Ofertas de compra |
| `CorrectionInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoiceReversal](CorrectionInvoiceReversal.md) |  | Anulación de factura de corrección de clientes |
| `CorrectionInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoice](CorrectionInvoice.md) |  | Factura de corrección de clientes |
| `PurchaseDeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDeliveryNotes](PurchaseDeliveryNotes.md) |  | Pedidos de entrada de mercancías |
| `CorrectionPurchaseInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoice](CorrectionPurchaseInvoice.md) |  | Factura de corrección de proveedores |
| `PickLists` | Collection([PickList](../Entidades/PickLists.md)) | [PickLists](PickLists.md) |  | Listas de picking |
| `InventoryGenEntries` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenEntries](InventoryGenEntries.md) |  | Entradas de mercancías |
| `BankPages` | Collection([BankPage](../Entidades/BankPages.md)) | [BankPages](BankPages.md) |  | Páginas de extracto bancario |
| `ScheduleJobService` | Collection([ScheduleJob](../Entidades/ScheduleJobService.md)) | [ScheduleJobService](ScheduleJobService.md) |  | Trabajos programados |
| `ServiceCalls` | Collection([ServiceCall](../Entidades/ServiceCalls.md)) | [ServiceCalls](ServiceCalls.md) |  | Llamadas de servicio |
| `EmployeesInfo` | Collection([EmployeeInfo](../Entidades/EmployeesInfo.md)) | [EmployeesInfo](EmployeesInfo.md) |  | Empleados |
| `Orders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Orders](Orders.md) |  | Pedidos de cliente (órdenes de venta) |
| `WizardPaymentMethods` | Collection([WizardPaymentMethod](../Entidades/WizardPaymentMethods.md)) | [WizardPaymentMethods](WizardPaymentMethods.md) |  | Vías de pago del asistente de pagos |
| `ServiceContracts` | Collection([ServiceContract](../Entidades/ServiceContracts.md)) | [ServiceContracts](ServiceContracts.md) |  | Contratos de servicio |
| `InventoryGenExits` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenExits](InventoryGenExits.md) |  | Salidas de mercancías |
| `MaterialRevaluation` | Collection([MaterialRevaluation](../Entidades/MaterialRevaluation.md)) | [MaterialRevaluation](MaterialRevaluation.md) |  | Revalorización de inventario |
| `Drafts` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Drafts](Drafts.md) |  | Borradores de documentos |
| `ApprovalRequests` | Collection([ApprovalRequest](../Entidades/ApprovalRequests.md)) | [ApprovalRequests](ApprovalRequests.md) |  | Solicitudes de autorización |
| `Queue` | Collection([Queue](../Entidades/Queue.md)) | [Queue](Queue.md) |  | Colas |
| `ReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [ReturnRequest](ReturnRequest.md) |  | Solicitudes de devolución de clientes |
| `DeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DeliveryNotes](DeliveryNotes.md) |  | Entregas |
| `Branch2` | [Branch](../Entidades/Branches.md) | [Branches](Branches.md) | Branch → Code | Sucursales |
| `Department2` | [Department](../Entidades/Departments.md) | [Departments](Departments.md) | Department → Code | Departamentos |
| `PurchaseInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseInvoices](PurchaseInvoices.md) |  | Facturas de proveedores |
| `SelfInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfInvoices](SelfInvoices.md) |  | Autofacturas |
| `SalesTaxAuthorities` | Collection([SalesTaxAuthority](../Entidades/SalesTaxAuthorities.md)) | [SalesTaxAuthorities](SalesTaxAuthorities.md) |  | Autoridades del impuesto sobre ventas |
| `Invoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Invoices](Invoices.md) |  | Facturas de clientes |
| `CreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CreditNotes](CreditNotes.md) |  | Notas de crédito de clientes |
| `SalesTaxAuthoritiesTypes` | Collection([SalesTaxAuthoritiesType](../Entidades/SalesTaxAuthoritiesTypes.md)) | [SalesTaxAuthoritiesTypes](SalesTaxAuthoritiesTypes.md) |  | Tipos de autoridades del impuesto sobre ventas |
| `KnowledgeBaseSolutions` | Collection([KnowledgeBaseSolution](../Entidades/KnowledgeBaseSolutions.md)) | [KnowledgeBaseSolutions](KnowledgeBaseSolutions.md) |  | Soluciones de la base de conocimiento |
| `Contacts` | Collection([Contact](../Entidades/Contacts.md)) | [Contacts](Contacts.md) |  | Contactos |
| `PurchaseCreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseCreditNotes](PurchaseCreditNotes.md) |  | Notas de crédito de proveedores |
| `ProductionOrders` | Collection([ProductionOrder](../Entidades/ProductionOrders.md)) | [ProductionOrders](ProductionOrders.md) |  | Órdenes de fabricación |
| `DownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DownPayments](DownPayments.md) |  | Facturas de anticipo de clientes |
| `PurchaseDownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDownPayments](PurchaseDownPayments.md) |  | Facturas de anticipo de proveedores |
| `PurchaseReturns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseReturns](PurchaseReturns.md) |  | Devoluciones de mercancías a proveedores |
| `Cockpits` | Collection([Cockpit](../Entidades/Cockpits.md)) | [Cockpits](Cockpits.md) |  | Cockpits |
| `UserPermissionTree` | Collection([UserPermissionTree](../Entidades/UserPermissionTree.md)) | [UserPermissionTree](UserPermissionTree.md) |  | Árbol de autorizaciones de usuario |
| `Activities` | Collection([Activity](../Entidades/Activities.md)) | [Activities](Activities.md) |  | Actividades |
| `PurchaseOrders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseOrders](PurchaseOrders.md) |  | Pedidos de compra (órdenes de compra) |
| `SelfCreditMemos` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfCreditMemos](SelfCreditMemos.md) |  | Autonotas de crédito |
| `Quotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Quotations](Quotations.md) |  | Ofertas de ventas (cotizaciones) |
| `Returns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Returns](Returns.md) |  | Devoluciones de clientes |
| `GoodsReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [GoodsReturnRequest](GoodsReturnRequest.md) |  | Solicitudes de devolución de mercancías |
| `SalesTaxCodes` | Collection([SalesTaxCode](../Entidades/SalesTaxCodes.md)) | [SalesTaxCodes](SalesTaxCodes.md) |  | Códigos del impuesto sobre ventas |
| `CorrectionPurchaseInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoiceReversal](CorrectionPurchaseInvoiceReversal.md) |  | Anulación de factura de corrección de proveedores |
| `PurchaseRequests` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseRequests](PurchaseRequests.md) |  | Solicitudes de compra |
| `FormPreferences` | Collection([ColumnPreferences](../Entidades/FormPreferences.md)) | [FormPreferences](FormPreferences.md) |  | Preferencias de formularios (columnas) |

## Bound actions (2)

### Close

- **Descripción (ES):** Cerrar
- **Request:** `POST /b1s/v2/Users(1)/Close`

### RemoveUserAndLicense

- **Descripción (ES):** Eliminar usuario y licencia
- **Request:** `POST /b1s/v2/Users(1)/RemoveUserAndLicense`


## Service operations that use this type

- [`UsersService_GetCurrentUser`](../Servicios/UsersService.md#usersservice_getcurrentuser)
