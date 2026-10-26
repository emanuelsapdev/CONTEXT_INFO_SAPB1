# SpecialPrices — Precios especiales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SpecialPrices`
- **Descripción (ES):** Precios especiales
- **Entity type:** `SpecialPrice` (open type: accepts dynamic/UDF properties)
- **Key:** `ItemCode` (Edm.String), `CardCode` (Edm.String)
- **DB tables (main / lines):** [OSPP](../../Tablas%20SAP%20B1/OSPP.md), [SPP1](../../Tablas%20SAP%20B1/SPP1.md), [SPP2](../../Tablas%20SAP%20B1/SPP2.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 12 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SpecialPrices?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SpecialPrices/$count` | Contar |
| Get by key | `GET /b1s/v2/SpecialPrices(ItemCode='value',CardCode='value')` | Obtener por clave |
| Create | `POST /b1s/v2/SpecialPrices` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SpecialPrices(ItemCode='value',CardCode='value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SpecialPrices(ItemCode='value',CardCode='value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/SpecialPrices(ItemCode='value',CardCode='value')` (only if the B1 object allows removal) | Borrar |

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ItemCode` 🔑 | Edm.String | No | Item Code | Código de artículo |
| 2 | `CardCode` 🔑 | Edm.String | No | Card Code | Código del socio de negocios |
| 3 | `Price` | Edm.Double | Yes | Price | Precio |
| 4 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 5 | `DiscountPercent` | Edm.Double | Yes | Discount Percent | Porcentaje de descuento |
| 6 | `PriceListNum` | Edm.Int32 | Yes | Price List Number | Número de lista de precios |
| 7 | `AutoUpdate` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Auto Update | Actualización automática |
| 8 | `SourcePrice` | [SourceCurrencyEnum](../Enums/SourceCurrencyEnum.md) | Yes | Source Price | Precio de origen |
| 9 | `Valid` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Valid | Válido (activo) |
| 10 | `ValidFrom` | Edm.DateTimeOffset | Yes | Valid From | Válido desde |
| 11 | `ValidTo` | Edm.DateTimeOffset | Yes | Valid To | Válido hasta |
| 12 | `SpecialPriceDataAreas` | Collection([SpecialPriceDataArea](../Tipos-Complejos/SpecialPriceDataArea.md)) | Yes | Special Price Data Areas | Rangos de fechas del precio especial |

## Navigation properties (3)

Use `GET /b1s/v2/SpecialPrices(ItemCode='value',CardCode='value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Item` | [Item](../Entidades/Items.md) | [Items](Items.md) | ItemCode → ItemCode | Artículos |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CardCode → CardCode | Socio de negocios |
| `PriceList` | [PriceList](../Entidades/PriceLists.md) | [PriceLists](PriceLists.md) | PriceListNum → PriceListNo | Lista de precios |
