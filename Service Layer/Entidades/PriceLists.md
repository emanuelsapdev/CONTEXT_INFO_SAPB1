# PriceLists — Listas de precios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `PriceLists`
- **Descripción (ES):** Listas de precios
- **Entity type:** `PriceList` (open type: accepts dynamic/UDF properties)
- **Key:** `PriceListNo` (Edm.Int32)
- **DB tables (main / lines):** [OPLN](../../Tablas%20SAP%20B1/OPLN.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 15 · **Navigation properties:** 6 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/PriceLists?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/PriceLists/$count` | Contar |
| Get by key | `GET /b1s/v2/PriceLists(1)` | Obtener por clave |
| Create | `POST /b1s/v2/PriceLists` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/PriceLists(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/PriceLists(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/PriceLists(1)` (only if the B1 object allows removal) | Borrar |

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `RoundingMethod` | [BoRoundingMethod](../Enums/BoRoundingMethod.md) | Yes | Rounding Method | Método de redondeo |
| 2 | `GroupNum` | [BoPriceListGroupNum](../Enums/BoPriceListGroupNum.md) | Yes | Group Number | Número de grupo (condiciones de pago) |
| 3 | `BasePriceList` | Edm.Int32 | Yes | Base Price List | Lista de precios base |
| 4 | `Factor` | Edm.Double | Yes | Factor | Factor |
| 5 | `PriceListNo` 🔑 | Edm.Int32 | No | Price List Number | Número de lista de precios |
| 6 | `PriceListName` | Edm.String | Yes | Price List Name | Nombre de la lista de precios |
| 7 | `IsGrossPrice` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Gross Price | Es precio bruto |
| 8 | `Active` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active | Activo |
| 9 | `ValidFrom` | Edm.DateTimeOffset | Yes | Valid From | Válido desde |
| 10 | `ValidTo` | Edm.DateTimeOffset | Yes | Valid To | Válido hasta |
| 11 | `DefaultPrimeCurrency` | Edm.String | Yes | Default Prime Currency | Moneda principal predeterminada |
| 12 | `DefaultAdditionalCurrency1` | Edm.String | Yes | Default Additional Currency 1 | Moneda adicional 1 predeterminada |
| 13 | `DefaultAdditionalCurrency2` | Edm.String | Yes | Default Additional Currency 2 | Moneda adicional 2 predeterminada |
| 14 | `RoundingRule` | [BoRoundingRule](../Enums/BoRoundingRule.md) | Yes | Rounding Rule | Regla de redondeo |
| 15 | `FixedAmount` | Edm.Double | Yes | Fixed Amount | Importe fijo |

## Navigation properties (6)

Use `GET /b1s/v2/PriceLists(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `StockTransfers` | Collection([StockTransfer](../Entidades/StockTransfers.md)) | [StockTransfers](StockTransfers.md) |  | Transferencias de stock |
| `ProductTrees` | Collection([ProductTree](../Entidades/ProductTrees.md)) | [ProductTrees](ProductTrees.md) |  | Listas de materiales (árbol de producto) |
| `BlanketAgreements` | Collection([BlanketAgreement](../Entidades/BlanketAgreements.md)) | [BlanketAgreements](BlanketAgreements.md) |  | Acuerdos globales |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
| `SpecialPrices` | Collection([SpecialPrice](../Entidades/SpecialPrices.md)) | [SpecialPrices](SpecialPrices.md) |  | Precios especiales |
| `PaymentTermsTypes` | Collection([PaymentTermsType](../Entidades/PaymentTermsTypes.md)) | [PaymentTermsTypes](PaymentTermsTypes.md) |  | Condiciones de pago |
