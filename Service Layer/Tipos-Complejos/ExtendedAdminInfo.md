# ExtendedAdminInfo — Información de administración ampliada

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ExtendedAdminInfo`
- **Descripción (ES):** Información de administración ampliada
- **Description (EN):** Extended Admin Information

- **Properties:** 38

## Properties (38)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AddressType` | Edm.String | Yes | Address Type | Tipo de dirección |
| 2 | `StreetNo` | Edm.String | Yes | Street Number | Número de calle |
| 3 | `STDCode` | Edm.Int32 | Yes | STD Code | Código STD |
| 4 | `STDCodeForeign` | Edm.Int32 | Yes | STD Code Foreign | Código STD (exterior) |
| 5 | `NatureOfCompanyCode` | Edm.Int32 | Yes | Nature Of Company Code | Código de naturaleza de la sociedad |
| 6 | `EconomicActivityTypeCode` | Edm.Int32 | Yes | Economic Activity Type Code | Código de tipo de actividad económica |
| 7 | `CreditContributionOriginCode` | Edm.String | Yes | Credit Contribution Origin Code | Código de origen de crédito de contribución |
| 8 | `IPIPeriodCode` | Edm.String | Yes | IPI Period Code | Código de período IPI |
| 9 | `CooperativeAssociationTypeCode` | Edm.Int32 | Yes | Cooperative Association Type Code | Código de tipo de asociación cooperativa |
| 10 | `ProfitTaxationCode` | Edm.Int32 | Yes | Profit Taxation Code | Código de tributación de beneficios |
| 11 | `CompanyQualificationCode` | Edm.Int32 | Yes | Company Qualification Code | Código de calificación de la sociedad |
| 12 | `DeclarerTypeCode` | Edm.Int32 | Yes | Declarer Type Code | Código de tipo de declarante |
| 13 | `IPITaxContributor` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | IPI Tax Contributor | Contribuyente de IPI |
| 14 | `CommercialRegister` | Edm.String | Yes | Commercial Register | Registro comercial |
| 15 | `DateOfIncorporation` | Edm.DateTimeOffset | Yes | Date Of Incorporation | Fecha de constitución |
| 16 | `SPEDProfile` | Edm.String | Yes | SPED Profile | Perfil SPED (Brasil) |
| 17 | `EnvironmentType` | Edm.Int32 | Yes | Environment Type | Tipo de entorno |
| 18 | `Opting4ICMS` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Opting 4 ICMS | Opción por ICMS |
| 19 | `OKDPNumber` | Edm.String | Yes | OKDP Number | Número OKDP (Rusia) |
| 20 | `GlobalLocationNumber` | Edm.String | Yes | Global Location Number | Número de localización global (GLN) |
| 21 | `EnableIntrastat` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Intrastat | Habilitar Intrastat |
| 22 | `AuthorityUser` | Edm.String | Yes | Authority User | Usuario de la autoridad |
| 23 | `AuthorityPassword` | Edm.String | Yes | Authority Password | Contraseña de la autoridad |
| 24 | `URLforGoodsTransportService` | Edm.String | Yes | UR Lfor Goods Transport Service | URL del servicio de transporte de mercancías |
| 25 | `URLforInvoiceTypeService` | Edm.String | Yes | UR Lfor Invoice Type Service | URL del servicio de tipo de factura |
| 26 | `ElectronicApprovalForGoodsTransEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Electronic Approval For Goods Trans Enabled | Autorización electrónica para transporte de mercancías habilitada |
| 27 | `ElectronicApprovalForInvoiceEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Electronic Approval For Invoice Enabled | Autorización electrónica para facturas habilitada |
| 28 | `AllowInactiveItemsInInventoryOpeningBalance` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allow Inactive Items In Inventory Opening Balance | Permitir artículos inactivos en saldo inicial de inventario |
| 29 | `AllowInactiveItemsInInventoryCountingAndPosting` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allow Inactive Items In Inventory Counting And Posting | Permitir artículos inactivos en recuento y contabilización de inventario |
| 30 | `AutoAssignNewBranchToBP` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Auto Assign New Branch To Business Partner | Asignar automáticamente nueva sucursal al socio de negocios |
| 31 | `DocumentRemarksInclude` | [DocumentRemarksIncludeTypeEnum](../Enums/DocumentRemarksIncludeTypeEnum.md) | Yes | Document Remarks Include | Incluir comentarios del documento |
| 32 | `CNPJOfIT` | Edm.String | Yes | CNPJ Of IT | CNPJ de TI |
| 33 | `CnPerson` | Edm.String | Yes | Cn Person | Persona de contacto |
| 34 | `Email` | Edm.String | Yes | Email | Correo electrónico |
| 35 | `Telephone` | Edm.String | Yes | Telephone | Teléfono |
| 36 | `NoWarningForLinkTypeUDF` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Number Warning For Link Type UDF | Sin advertencia para UDF de tipo vínculo |
| 37 | `EnableSameURLforPaymentTypeService` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Same UR Lfor Payment Type Service | Habilitar misma URL para servicio de tipo de pago |
| 38 | `CopyRefDocFormOrigDocToDupDoc` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Copy Ref Document Form Orig Document To Dup Document | Copiar documento de referencia del original al duplicado |

## Used by (properties)

- [AdminInfo](AdminInfo.md).`ExtendedAdminInfo`
