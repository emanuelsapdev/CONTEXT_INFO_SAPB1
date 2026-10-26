# BPAddress — Dirección del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BPAddress`
- **Descripción (ES):** Dirección del socio de negocios
- **Description (EN):** Business Partner Address
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 27

## Properties (27)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AddressName` | Edm.String | Yes | Address Name | Nombre de dirección |
| 2 | `Street` | Edm.String | Yes | Street | Calle |
| 3 | `Block` | Edm.String | Yes | Block | Barrio/bloque |
| 4 | `ZipCode` | Edm.String | Yes | Zip Code | Código postal |
| 5 | `City` | Edm.String | Yes | City | Ciudad |
| 6 | `County` | Edm.String | Yes | County | Condado |
| 7 | `Country` | Edm.String | Yes | Country | País |
| 8 | `State` | Edm.String | Yes | State | Estado/provincia |
| 9 | `FederalTaxID` | Edm.String | Yes | Federal Tax ID | CUIT / ID fiscal federal |
| 10 | `TaxCode` | Edm.String | Yes | Tax Code | Indicador de impuesto |
| 11 | `BuildingFloorRoom` | Edm.String | Yes | Building Floor Room | Edificio/piso/oficina |
| 12 | `AddressType` | [BoAddressType](../Enums/BoAddressType.md) | Yes | Address Type | Tipo de dirección |
| 13 | `AddressName2` | Edm.String | Yes | Address Name 2 | Nombre de dirección 2 |
| 14 | `AddressName3` | Edm.String | Yes | Address Name 3 | Nombre de dirección 3 |
| 15 | `TypeOfAddress` | Edm.String | Yes | Type Of Address | Tipo de dirección |
| 16 | `StreetNo` | Edm.String | Yes | Street Number | Número de calle |
| 17 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 18 | `RowNum` | Edm.Int32 | Yes | Row Number | Número de línea |
| 19 | `GlobalLocationNumber` | Edm.String | Yes | Global Location Number | Número de localización global (GLN) |
| 20 | `Nationality` | Edm.String | Yes | Nationality | Nacionalidad |
| 21 | `TaxOffice` | Edm.String | Yes | Tax Office | Oficina tributaria |
| 22 | `GSTIN` | Edm.String | Yes | GSTIN | GSTIN (India) |
| 23 | `GstType` | [BoGSTRegnTypeEnum](../Enums/BoGSTRegnTypeEnum.md) | Yes | Gst Type | Tipo de GST |
| 24 | `CreateDate` | Edm.DateTimeOffset | Yes | Create Date | Fecha de creación |
| 25 | `CreateTime` | Edm.TimeOfDay | Yes | Create Time | Hora de creación |
| 26 | `MYFType` | [BoMYFTypeEnum](../Enums/BoMYFTypeEnum.md) | Yes | MYF Type | Tipo MYF |
| 27 | `TaasEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Taas Enabled | TaaS habilitado |

## Used by (properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`BPAddresses`
