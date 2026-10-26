# GLAccountAdvancedRuleParams — Parámetros de reglas avanzadas de cuentas de mayor

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `GLAccountAdvancedRuleParams`
- **Descripción (ES):** Parámetros de reglas avanzadas de cuentas de mayor
- **Description (EN):** G/L Account Advanced Rule Parameters

- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsoluteEntry` | Edm.Int32 | Yes | Absolute Entry | Entrada absoluta (ID interno) |
| 2 | `Period` | Edm.String | Yes | Period | Período |
| 3 | `Code` | Edm.String | Yes | Code | Código |
| 4 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 5 | `ItemGroup` | Edm.Int32 | Yes | Item Group | Grupo de artículos |
| 6 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |
| 7 | `BPGroup` | Edm.Int32 | Yes | Business Partner Group | Grupo de socios de negocios |
| 8 | `FederalTaxID` | Edm.String | Yes | Federal Tax ID | CUIT / ID fiscal federal |
| 9 | `ShipToCountry` | Edm.String | Yes | Ship To Country | País de envío |
| 10 | `ShipToState` | Edm.String | Yes | Ship To State | Estado/provincia de envío |

## Used by (service operations)

- [`GLAccountAdvancedRulesService_GetList`](../Servicios/GLAccountAdvancedRulesService.md#glaccountadvancedrulesservice_getlist)
