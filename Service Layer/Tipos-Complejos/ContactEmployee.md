# ContactEmployee — Personas de contacto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ContactEmployee`
- **Descripción (ES):** Personas de contacto
- **Description (EN):** Contact Employee
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 35

## Properties (35)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Position` | Edm.String | Yes | Position | Posición/cargo |
| 4 | `Address` | Edm.String | Yes | Address | Dirección |
| 5 | `Phone1` | Edm.String | Yes | Phone 1 | Teléfono 1 |
| 6 | `Phone2` | Edm.String | Yes | Phone 2 | Teléfono 2 |
| 7 | `MobilePhone` | Edm.String | Yes | Mobile Phone | Teléfono celular |
| 8 | `Fax` | Edm.String | Yes | Fax | Fax |
| 9 | `E_Mail` | Edm.String | Yes | E Mail | Correo electrónico |
| 10 | `Pager` | Edm.String | Yes | Pager | Buscapersonas |
| 11 | `Remarks1` | Edm.String | Yes | Remarks 1 | Comentarios 1 |
| 12 | `Remarks2` | Edm.String | Yes | Remarks 2 | Comentarios 2 |
| 13 | `Password` | Edm.String | Yes | Password | Contraseña |
| 14 | `InternalCode` | Edm.Int32 | Yes | Internal Code | Código interno |
| 15 | `PlaceOfBirth` | Edm.String | Yes | Place Of Birth | Lugar de nacimiento |
| 16 | `DateOfBirth` | Edm.DateTimeOffset | Yes | Date Of Birth | Fecha de nacimiento |
| 17 | `Gender` | [BoGenderTypes](../Enums/BoGenderTypes.md) | Yes | Gender | Sexo |
| 18 | `Profession` | Edm.String | Yes | Profession | Profesión |
| 19 | `Title` | Edm.String | Yes | Title | Título |
| 20 | `CityOfBirth` | Edm.String | Yes | City Of Birth | Ciudad de nacimiento |
| 21 | `Active` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active | Activo |
| 22 | `FirstName` | Edm.String | Yes | First Name | Nombre |
| 23 | `MiddleName` | Edm.String | Yes | Middle Name | Segundo nombre |
| 24 | `LastName` | Edm.String | Yes | Last Name | Apellido |
| 25 | `EmailGroupCode` | Edm.String | Yes | Email Group Code | Código de grupo de correo |
| 26 | `BlockSendingMarketingContent` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Sending Marketing Content | Bloquear envío de contenido de marketing |
| 27 | `CreateDate` | Edm.DateTimeOffset | Yes | Create Date | Fecha de creación |
| 28 | `CreateTime` | Edm.TimeOfDay | Yes | Create Time | Hora de creación |
| 29 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 30 | `UpdateTime` | Edm.TimeOfDay | Yes | Update Time | Hora de actualización |
| 31 | `ConnectedAddressName` | Edm.String | Yes | Connected Address Name | Nombre de dirección vinculada |
| 32 | `ConnectedAddressType` | [BoAddressType](../Enums/BoAddressType.md) | Yes | Connected Address Type | Tipo de dirección vinculada |
| 33 | `ForeignCountry` | Edm.String | Yes | Foreign Country | País extranjero |
| 34 | `GenderEx` | Edm.String | Yes | Gender Ex | Sexo (ampliado) |
| 35 | `ContactEmployeeBlockSendingMarketingContents` | Collection([ContactEmployeeBlockSendingMarketingContent](../Tipos-Complejos/ContactEmployeeBlockSendingMarketingContent.md)) | Yes | Contact Employee Block Sending Marketing Contents | Bloqueos de envío de marketing de la persona de contacto |

## Used by (properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`ContactEmployees`
