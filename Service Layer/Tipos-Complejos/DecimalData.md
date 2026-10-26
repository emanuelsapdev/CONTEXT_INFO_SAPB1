# DecimalData — Datos decimales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DecimalData`
- **Descripción (ES):** Datos decimales
- **Description (EN):** Decimal Data

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Value` | Edm.Double | Yes | Value | Valor |
| 2 | `Context` | [RoundingContextEnum](../Enums/RoundingContextEnum.md) | Yes | Context | Contexto |
| 3 | `Currency` | Edm.String | Yes | Currency | Moneda |

## Used by (service operations)

- [`CompanyService_RoundDecimal`](../Servicios/CompanyService.md#companyservice_rounddecimal)
