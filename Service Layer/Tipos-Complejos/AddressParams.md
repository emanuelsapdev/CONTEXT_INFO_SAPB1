# AddressParams — Parámetros de dirección

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AddressParams`
- **Descripción (ES):** Parámetros de dirección
- **Description (EN):** Address Parameters
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 13

## Properties (13)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Country` | Edm.String | Yes | Country | País |
| 2 | `State` | Edm.String | Yes | State | Estado/provincia |
| 3 | `County` | Edm.String | Yes | County | Condado |
| 4 | `ZipCode` | Edm.String | Yes | Zip Code | Código postal |
| 5 | `City` | Edm.String | Yes | City | Ciudad |
| 6 | `Building` | Edm.String | Yes | Building | Edificio |
| 7 | `Block` | Edm.String | Yes | Block | Barrio/bloque |
| 8 | `Street` | Edm.String | Yes | Street | Calle |
| 9 | `StreetNo` | Edm.String | Yes | Street Number | Número de calle |
| 10 | `Address2` | Edm.String | Yes | Address 2 | Dirección 2 |
| 11 | `Address3` | Edm.String | Yes | Address 3 | Dirección 3 |
| 12 | `AddressType` | Edm.String | Yes | Address Type | Tipo de dirección |
| 13 | `GlobalLocationNumber` | Edm.String | Yes | Global Location Number | Número de localización global (GLN) |

## Used by (service operations)

- [`AddressService_GetFullAddress`](../Servicios/AddressService.md#addressservice_getfulladdress)
