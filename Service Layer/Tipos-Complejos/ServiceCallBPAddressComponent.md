# ServiceCallBPAddressComponent — Componentes de dirección del socio de negocios de la llamada

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ServiceCallBPAddressComponent`
- **Descripción (ES):** Componentes de dirección del socio de negocios de la llamada
- **Description (EN):** Service Call Business Partner Address Component
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 26

## Properties (26)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ShipToStreet` | Edm.String | Yes | Ship To Street | Calle de envío |
| 2 | `ShipToStreetNo` | Edm.String | Yes | Ship To Street Number | Número de calle de envío |
| 3 | `ShipToBlock` | Edm.String | Yes | Ship To Block | Barrio de envío |
| 4 | `ShipToBuilding` | Edm.String | Yes | Ship To Building | Edificio de envío |
| 5 | `ShipToCity` | Edm.String | Yes | Ship To City | Ciudad de envío |
| 6 | `ShipToZipCode` | Edm.String | Yes | Ship To Zip Code | Código postal de envío |
| 7 | `ShipToState` | Edm.String | Yes | Ship To State | Estado/provincia de envío |
| 8 | `ShipToCounty` | Edm.String | Yes | Ship To County | Condado de envío |
| 9 | `ShipToCountry` | Edm.String | Yes | Ship To Country | País de envío |
| 10 | `ShipToAddressType` | Edm.String | Yes | Ship To Address Type | Tipo de dirección de envío |
| 11 | `ShipToAddress2` | Edm.String | Yes | Ship To Address 2 | Dirección de envío 2 |
| 12 | `ShipToAddress3` | Edm.String | Yes | Ship To Address 3 | Dirección de envío 3 |
| 13 | `ShipToGlobalLocationNumber` | Edm.String | Yes | Ship To Global Location Number | GLN de envío |
| 14 | `BillToStreet` | Edm.String | Yes | Bill To Street | Calle de facturación |
| 15 | `BillToStreetNo` | Edm.String | Yes | Bill To Street Number | Número de calle de facturación |
| 16 | `BillToBlock` | Edm.String | Yes | Bill To Block | Barrio de facturación |
| 17 | `BillToBuilding` | Edm.String | Yes | Bill To Building | Edificio de facturación |
| 18 | `BillToCity` | Edm.String | Yes | Bill To City | Ciudad de facturación |
| 19 | `BillToZipCode` | Edm.String | Yes | Bill To Zip Code | Código postal de facturación |
| 20 | `BillToState` | Edm.String | Yes | Bill To State | Estado/provincia de facturación |
| 21 | `BillToCounty` | Edm.String | Yes | Bill To County | Condado de facturación |
| 22 | `BillToCountry` | Edm.String | Yes | Bill To Country | País de facturación |
| 23 | `BillToAddressType` | Edm.String | Yes | Bill To Address Type | Tipo de dirección de facturación |
| 24 | `BillToAddress2` | Edm.String | Yes | Bill To Address 2 | Dirección de facturación 2 |
| 25 | `BillToAddress3` | Edm.String | Yes | Bill To Address 3 | Dirección de facturación 3 |
| 26 | `BillToGlobalLocationNumber` | Edm.String | Yes | Bill To Global Location Number | GLN de facturación |

## Used by (properties)

- [ServiceCall](../Entidades/ServiceCalls.md).`ServiceCallBPAddressComponents`
