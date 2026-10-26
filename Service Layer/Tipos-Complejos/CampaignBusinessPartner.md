# CampaignBusinessPartner — Socios de negocios de la campaña

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CampaignBusinessPartner`
- **Descripción (ES):** Socios de negocios de la campaña
- **Description (EN):** Campaign Business Partner
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 42

## Properties (42)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CampaignNumber` | Edm.Int32 | Yes | Campaign Number | Número de campaña |
| 2 | `CampaignLineNumber` | Edm.Int32 | Yes | Campaign Line Number | Número de línea de la campaña |
| 3 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 4 | `BPName` | Edm.String | Yes | Business Partner Name | Nombre del socio de negocios |
| 5 | `BPGroupName` | Edm.String | Yes | Business Partner Group Name | Nombre del grupo de socios de negocios |
| 6 | `BPIndustryName` | Edm.String | Yes | Business Partner Industry Name | Ramo del socio de negocios |
| 7 | `BPStatus` | Edm.String | Yes | Business Partner Status | Estado del socio de negocios |
| 8 | `ContactCode` | Edm.String | Yes | Contact Code | Código de contacto |
| 9 | `ContactTitle` | Edm.String | Yes | Contact Title | Título del contacto |
| 10 | `ContactPosition` | Edm.String | Yes | Contact Position | Cargo del contacto |
| 11 | `ContactEmail` | Edm.String | Yes | Contact Email | Correo del contacto |
| 12 | `ContactTelephone` | Edm.String | Yes | Contact Telephone | Teléfono del contacto |
| 13 | `ContactMobile` | Edm.String | Yes | Contact Mobile | Celular del contacto |
| 14 | `ContactFax` | Edm.String | Yes | Contact Fax | Fax del contacto |
| 15 | `ContactAddress` | Edm.String | Yes | Contact Address | Dirección del contacto |
| 16 | `Response` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Response | Respuesta |
| 17 | `RelatedSalesOpportunity` | Edm.Int32 | Yes | Related Sales Opportunity | Oportunidad de venta relacionada |
| 18 | `Street` | Edm.String | Yes | Street | Calle |
| 19 | `Block` | Edm.String | Yes | Block | Barrio/bloque |
| 20 | `City` | Edm.String | Yes | City | Ciudad |
| 21 | `ZipCode` | Edm.String | Yes | Zip Code | Código postal |
| 22 | `County` | Edm.String | Yes | County | Condado |
| 23 | `State` | Edm.String | Yes | State | Estado/provincia |
| 24 | `Country` | Edm.String | Yes | Country | País |
| 25 | `Building` | Edm.String | Yes | Building | Edificio |
| 26 | `DocType` | [LinkedDocTypeEnum](../Enums/LinkedDocTypeEnum.md) | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 27 | `IsShowLinkedDoc` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Show Linked Document | Mostrar documento vinculado |
| 28 | `DocNumber` | Edm.Int32 | Yes | Document Number | Número de documento |
| 29 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 30 | `FirstName` | Edm.String | Yes | First Name | Nombre |
| 31 | `MiddleName` | Edm.String | Yes | Middle Name | Segundo nombre |
| 32 | `LastName` | Edm.String | Yes | Last Name | Apellido |
| 33 | `AddressID` | Edm.String | Yes | Address ID | ID de dirección |
| 34 | `AddressType` | Edm.String | Yes | Address Type | Tipo de dirección |
| 35 | `AddressName2` | Edm.String | Yes | Address Name 2 | Nombre de dirección 2 |
| 36 | `AddressName3` | Edm.String | Yes | Address Name 3 | Nombre de dirección 3 |
| 37 | `FederalTaxID` | Edm.String | Yes | Federal Tax ID | CUIT / ID fiscal federal |
| 38 | `StreetNo` | Edm.String | Yes | Street Number | Número de calle |
| 39 | `CreateActivity` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Create Activity | Crear actividad |
| 40 | `AssignTo` | [CampaignAssignToEnum](../Enums/CampaignAssignToEnum.md) | Yes | Assign To | Asignar a |
| 41 | `AssignName` | Edm.Int32 | Yes | Assign Name | Nombre asignado |
| 42 | `ResponseType` | Edm.String | Yes | Response Type | Tipo de respuesta |

## Used by (properties)

- [Campaign](../Entidades/Campaigns.md).`CampaignBusinessPartners`
