# CustomerEquipmentCards — Tarjetas de equipo del cliente

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `CustomerEquipmentCards`
- **Descripción (ES):** Tarjetas de equipo del cliente
- **Entity type:** `CustomerEquipmentCard` (open type: accepts dynamic/UDF properties)
- **Key:** `EquipmentCardNum` (Edm.Int32)
- **DB tables (main / lines):** [OINS](../../Tablas%20SAP%20B1/OINS.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 39 · **Navigation properties:** 7 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/CustomerEquipmentCards?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/CustomerEquipmentCards/$count` | Contar |
| Get by key | `GET /b1s/v2/CustomerEquipmentCards(1)` | Obtener por clave |
| Create | `POST /b1s/v2/CustomerEquipmentCards` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/CustomerEquipmentCards(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/CustomerEquipmentCards(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/CustomerEquipmentCards(1)` (only if the B1 object allows removal) | Borrar |

## Properties (39)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `EquipmentCardNum` 🔑 | Edm.Int32 | No | Equipment Card Number | Número de tarjeta de equipo |
| 2 | `CustomerCode` | Edm.String | Yes | Customer Code | Código de cliente |
| 3 | `CustomerName` | Edm.String | Yes | Customer Name | Nombre del cliente |
| 4 | `ContactEmployeeCode` | Edm.Int32 | Yes | Contact Employee Code | Código de persona de contacto |
| 5 | `DirectCustomerCode` | Edm.String | Yes | Direct Customer Code | Código de cliente directo |
| 6 | `DirectCustomerName` | Edm.String | Yes | Direct Customer Name | Nombre de cliente directo |
| 7 | `ManufacturerSerialNum` | Edm.String | Yes | Manufacturer Serial Number | Número de serie del fabricante |
| 8 | `InternalSerialNum` | Edm.String | Yes | Internal Serial Number | Número de serie interno |
| 9 | `RequiredResolutionTime` | Edm.Int32 | Yes | Required Resolution Time | Tiempo de resolución requerido |
| 10 | `RequiredResolutionUnit` | [BoResolutionUnits](../Enums/BoResolutionUnits.md) | Yes | Required Resolution Unit | Unidad de tiempo de resolución requerida |
| 11 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 12 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 13 | `InvoiceCode` | Edm.Int32 | Yes | Invoice Code | Código de factura |
| 14 | `InvoiceNumber` | Edm.Int32 | Yes | Invoice Number | Número de factura |
| 15 | `DeliveryDate` | Edm.DateTimeOffset | Yes | Delivery Date | Fecha de entrega |
| 16 | `ContactPhone` | Edm.String | Yes | Contact Phone | Teléfono del contacto |
| 17 | `Street` | Edm.String | Yes | Street | Calle |
| 18 | `Block` | Edm.String | Yes | Block | Barrio/bloque |
| 19 | `ZipCode` | Edm.String | Yes | Zip Code | Código postal |
| 20 | `City` | Edm.String | Yes | City | Ciudad |
| 21 | `County` | Edm.String | Yes | County | Condado |
| 22 | `CountryCode` | Edm.String | Yes | Country Code | Código de país |
| 23 | `StateCode` | Edm.String | Yes | State Code | Código de estado/provincia |
| 24 | `InstallLocation` | Edm.String | Yes | Install Location | Ubicación de instalación |
| 25 | `ContractCode` | Edm.Int32 | Yes | Contract Code | Código de contrato |
| 26 | `ContractStartDate` | Edm.DateTimeOffset | Yes | Contract Start Date | Fecha de inicio del contrato |
| 27 | `ContractEndDate` | Edm.DateTimeOffset | Yes | Contract End Date | Fecha de fin del contrato |
| 28 | `DeliveryCode` | Edm.Int32 | Yes | Delivery Code | Código de entrega |
| 29 | `DeliveryNumber` | Edm.Int32 | Yes | Delivery Number | Número de entrega |
| 30 | `StatusOfSerialNumber` | [BoSerialNumberStatus](../Enums/BoSerialNumberStatus.md) | Yes | Status Of Serial Number | Estado del número de serie |
| 31 | `ReplaceSN` | Edm.Int32 | Yes | Replace SN | Reemplazar número de serie |
| 32 | `DefaultTechnician` | Edm.Int32 | Yes | Default Technician | Técnico predeterminado |
| 33 | `ReplacedBySN` | Edm.Int32 | Yes | Replaced By SN | Reemplazado por número de serie |
| 34 | `Defaultterritory` | Edm.Int32 | Yes | Defaultterritory | Territorio predeterminado |
| 35 | `BuildingFloorRoom` | Edm.String | Yes | Building Floor Room | Edificio/piso/oficina |
| 36 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 37 | `StreetNo` | Edm.String | Yes | Street Number | Número de calle |
| 38 | `ServiceBPType` | [BoEquipmentBPType](../Enums/BoEquipmentBPType.md) | Yes | Service Business Partner Type | Tipo de socio de negocios del servicio |
| 39 | `CustomerEquipmentCardBusinessPartners` | Collection([CustomerEquipmentCardBusinessPartner](../Tipos-Complejos/CustomerEquipmentCardBusinessPartner.md)) | Yes | Customer Equipment Card Business Partners | Socios de negocios de la tarjeta de equipo |

## Navigation properties (7)

Use `GET /b1s/v2/CustomerEquipmentCards(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CustomerCode → CardCode | Socio de negocios |
| `Item` | [Item](../Entidades/Items.md) | [Items](Items.md) | ItemCode → ItemCode | Artículos |
| `Country` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | CountryCode → Code | País |
| `ServiceContract` | [ServiceContract](../Entidades/ServiceContracts.md) | [ServiceContracts](ServiceContracts.md) | ContractCode → ContractID | Contratos de servicio |
| `EmployeeInfo` | [EmployeeInfo](../Entidades/EmployeesInfo.md) | [EmployeesInfo](EmployeesInfo.md) | DefaultTechnician → EmployeeID | Empleados |
| `Territory` | [Territory](../Entidades/Territories.md) | [Territories](Territories.md) | Defaultterritory → TerritoryID | Territorio |
| `Attachments2` | [Attachments2](../Entidades/Attachments2.md) | [Attachments2](Attachments2.md) | AttachmentEntry → AbsoluteEntry | Anexos |
