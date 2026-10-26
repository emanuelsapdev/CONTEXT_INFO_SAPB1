# AdvancedGLAccountParams — Parámetros de cuenta de mayor avanzada

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AdvancedGLAccountParams`
- **Descripción (ES):** Parámetros de cuenta de mayor avanzada
- **Description (EN):** Advanced G/L Account Parameters

- **Properties:** 15

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 2 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |
| 3 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 4 | `FederalTaxID` | Edm.String | Yes | Federal Tax ID | CUIT / ID fiscal federal |
| 5 | `ShipToCountry` | Edm.String | Yes | Ship To Country | País de envío |
| 6 | `ShipToState` | Edm.String | Yes | Ship To State | Estado/provincia de envío |
| 7 | `VatGroup` | Edm.String | Yes | Vat Group | Grupo de IVA (indicador de impuesto) |
| 8 | `PostingDate` | Edm.DateTimeOffset | Yes | Posting Date | Fecha de contabilización |
| 9 | `AccountType` | [InventoryAccountTypeEnum](../Enums/InventoryAccountTypeEnum.md) | Yes | Account Type | Tipo de cuenta |
| 10 | `Usage` | Edm.Int32 | Yes | Usage | Uso |
| 11 | `UDF1` | Edm.String | Yes | UDF 1 | UDF 1 |
| 12 | `UDF2` | Edm.String | Yes | UDF 2 | UDF 2 |
| 13 | `UDF3` | Edm.String | Yes | UDF 3 | UDF 3 |
| 14 | `UDF4` | Edm.String | Yes | UDF 4 | UDF 4 |
| 15 | `UDF5` | Edm.String | Yes | UDF 5 | UDF 5 |

## Used by (service operations)

- [`CompanyService_GetAdvancedGLAccount`](../Servicios/CompanyService.md#companyservice_getadvancedglaccount)
