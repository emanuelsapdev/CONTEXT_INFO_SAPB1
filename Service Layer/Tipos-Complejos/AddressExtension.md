# AddressExtension — Extensión de dirección

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AddressExtension`
- **Descripción (ES):** Extensión de dirección
- **Description (EN):** Address Extension
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 74

## Properties (74)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ShipToStreet` | Edm.String | Yes | Ship To Street | Calle de envío |
| 2 | `ShipToStreetNo` | Edm.String | Yes | Ship To Street Number | Número de calle de envío |
| 3 | `ShipToBlock` | Edm.String | Yes | Ship To Block | Barrio de envío |
| 4 | `ShipToBuilding` | Edm.String | Yes | Ship To Building | Edificio de envío |
| 5 | `ShipToCity` | Edm.String | Yes | Ship To City | Ciudad de envío |
| 6 | `ShipToZipCode` | Edm.String | Yes | Ship To Zip Code | Código postal de envío |
| 7 | `ShipToCounty` | Edm.String | Yes | Ship To County | Condado de envío |
| 8 | `ShipToState` | Edm.String | Yes | Ship To State | Estado/provincia de envío |
| 9 | `ShipToCountry` | Edm.String | Yes | Ship To Country | País de envío |
| 10 | `ShipToAddressType` | Edm.String | Yes | Ship To Address Type | Tipo de dirección de envío |
| 11 | `BillToStreet` | Edm.String | Yes | Bill To Street | Calle de facturación |
| 12 | `BillToStreetNo` | Edm.String | Yes | Bill To Street Number | Número de calle de facturación |
| 13 | `BillToBlock` | Edm.String | Yes | Bill To Block | Barrio de facturación |
| 14 | `BillToBuilding` | Edm.String | Yes | Bill To Building | Edificio de facturación |
| 15 | `BillToCity` | Edm.String | Yes | Bill To City | Ciudad de facturación |
| 16 | `BillToZipCode` | Edm.String | Yes | Bill To Zip Code | Código postal de facturación |
| 17 | `BillToCounty` | Edm.String | Yes | Bill To County | Condado de facturación |
| 18 | `BillToState` | Edm.String | Yes | Bill To State | Estado/provincia de facturación |
| 19 | `BillToCountry` | Edm.String | Yes | Bill To Country | País de facturación |
| 20 | `BillToAddressType` | Edm.String | Yes | Bill To Address Type | Tipo de dirección de facturación |
| 21 | `ShipToGlobalLocationNumber` | Edm.String | Yes | Ship To Global Location Number | GLN de envío |
| 22 | `BillToGlobalLocationNumber` | Edm.String | Yes | Bill To Global Location Number | GLN de facturación |
| 23 | `ShipToAddress2` | Edm.String | Yes | Ship To Address 2 | Dirección de envío 2 |
| 24 | `ShipToAddress3` | Edm.String | Yes | Ship To Address 3 | Dirección de envío 3 |
| 25 | `BillToAddress2` | Edm.String | Yes | Bill To Address 2 | Dirección de facturación 2 |
| 26 | `BillToAddress3` | Edm.String | Yes | Bill To Address 3 | Dirección de facturación 3 |
| 27 | `PlaceOfSupply` | Edm.String | Yes | Place Of Supply | Lugar de suministro |
| 28 | `PurchasePlaceOfSupply` | Edm.String | Yes | Purchase Place Of Supply | Lugar de suministro de compra |
| 29 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 30 | `GoodsIssuePlaceBP` | Edm.String | Yes | Goods Issue Place Business Partner | Socio de negocios del lugar de salida |
| 31 | `GoodsIssuePlaceCNPJ` | Edm.String | Yes | Goods Issue Place CNPJ | CNPJ del lugar de salida |
| 32 | `GoodsIssuePlaceCPF` | Edm.String | Yes | Goods Issue Place CPF | CPF del lugar de salida |
| 33 | `GoodsIssuePlaceStreet` | Edm.String | Yes | Goods Issue Place Street | Calle del lugar de salida |
| 34 | `GoodsIssuePlaceStreetNo` | Edm.String | Yes | Goods Issue Place Street Number | Número de calle del lugar de salida |
| 35 | `GoodsIssuePlaceBuilding` | Edm.String | Yes | Goods Issue Place Building | Edificio del lugar de salida |
| 36 | `GoodsIssuePlaceZip` | Edm.String | Yes | Goods Issue Place Zip | Código postal del lugar de salida |
| 37 | `GoodsIssuePlaceBlock` | Edm.String | Yes | Goods Issue Place Block | Barrio del lugar de salida de mercancías |
| 38 | `GoodsIssuePlaceCity` | Edm.String | Yes | Goods Issue Place City | Ciudad del lugar de salida |
| 39 | `GoodsIssuePlaceCounty` | Edm.String | Yes | Goods Issue Place County | Condado del lugar de salida |
| 40 | `GoodsIssuePlaceState` | Edm.String | Yes | Goods Issue Place State | Estado del lugar de salida |
| 41 | `GoodsIssuePlaceCountry` | Edm.String | Yes | Goods Issue Place Country | País del lugar de salida |
| 42 | `GoodsIssuePlacePhone` | Edm.String | Yes | Goods Issue Place Phone | Teléfono del lugar de salida |
| 43 | `GoodsIssuePlaceEMail` | Edm.String | Yes | Goods Issue Place E Mail | Correo del lugar de salida |
| 44 | `GoodsIssuePlaceDepartureDate` | Edm.DateTimeOffset | Yes | Goods Issue Place Departure Date | Fecha de salida del lugar de salida |
| 45 | `DeliveryPlaceBP` | Edm.String | Yes | Delivery Place Business Partner | Socio de negocios del lugar de entrega |
| 46 | `DeliveryPlaceCNPJ` | Edm.String | Yes | Delivery Place CNPJ | CNPJ del lugar de entrega |
| 47 | `DeliveryPlaceCPF` | Edm.String | Yes | Delivery Place CPF | CPF del lugar de entrega |
| 48 | `DeliveryPlaceStreet` | Edm.String | Yes | Delivery Place Street | Calle del lugar de entrega |
| 49 | `DeliveryPlaceStreetNo` | Edm.String | Yes | Delivery Place Street Number | Número de calle del lugar de entrega |
| 50 | `DeliveryPlaceBuilding` | Edm.String | Yes | Delivery Place Building | Edificio del lugar de entrega |
| 51 | `DeliveryPlaceZip` | Edm.String | Yes | Delivery Place Zip | Código postal del lugar de entrega |
| 52 | `DeliveryPlaceBlock` | Edm.String | Yes | Delivery Place Block | Barrio del lugar de entrega |
| 53 | `DeliveryPlaceCity` | Edm.String | Yes | Delivery Place City | Ciudad del lugar de entrega |
| 54 | `DeliveryPlaceCounty` | Edm.String | Yes | Delivery Place County | Condado del lugar de entrega |
| 55 | `DeliveryPlaceState` | Edm.String | Yes | Delivery Place State | Estado del lugar de entrega |
| 56 | `DeliveryPlaceCountry` | Edm.String | Yes | Delivery Place Country | País del lugar de entrega |
| 57 | `DeliveryPlacePhone` | Edm.String | Yes | Delivery Place Phone | Teléfono del lugar de entrega |
| 58 | `DeliveryPlaceEMail` | Edm.String | Yes | Delivery Place E Mail | Correo del lugar de entrega |
| 59 | `DeliveryPlaceDepartureDate` | Edm.DateTimeOffset | Yes | Delivery Place Departure Date | Fecha de salida del lugar de entrega |
| 60 | `ShipToStreetForReturn` | Edm.String | Yes | Ship To Street For Return | Calle de envío para devolución |
| 61 | `ShipToStreetNoForReturn` | Edm.String | Yes | Ship To Street Number For Return | Número de calle de envío para devolución |
| 62 | `ShipToBlockForReturn` | Edm.String | Yes | Ship To Block For Return | Barrio de envío para devolución |
| 63 | `ShipToBuildingForReturn` | Edm.String | Yes | Ship To Building For Return | Edificio de envío para devolución |
| 64 | `ShipToCityForReturn` | Edm.String | Yes | Ship To City For Return | Ciudad de envío para devolución |
| 65 | `ShipToZipCodeForReturn` | Edm.String | Yes | Ship To Zip Code For Return | Código postal de envío para devolución |
| 66 | `ShipToCountyForReturn` | Edm.String | Yes | Ship To County For Return | Condado de envío para devolución |
| 67 | `ShipToStateForReturn` | Edm.String | Yes | Ship To State For Return | Estado de envío para devolución |
| 68 | `ShipToCountryForReturn` | Edm.String | Yes | Ship To Country For Return | País de envío para devolución |
| 69 | `ShipToAddressTypeForReturn` | Edm.String | Yes | Ship To Address Type For Return | Tipo de dirección de envío para devolución |
| 70 | `ShipToGlobalLocationNumberForReturn` | Edm.String | Yes | Ship To Global Location Number For Return | GLN de envío para devolución |
| 71 | `ShipToAddress2ForReturn` | Edm.String | Yes | Ship To Address 2 For Return | Dirección de envío 2 para devolución |
| 72 | `ShipToAddress3ForReturn` | Edm.String | Yes | Ship To Address 3 For Return | Dirección de envío 3 para devolución |
| 73 | `U_B1SYS_TrailerId` | Edm.String | Yes | [AR localization] Trailer ID | [Loc. AR] Patente del acoplado/remolque |
| 74 | `U_B1SYS_IncotermsTxt` | Edm.String | Yes | [AR localization] Incoterms Txt | [Loc. AR] Texto de Incoterms |

## Used by (properties)

- [Document](../Entidades/PurchaseQuotations.md).`AddressExtension`
