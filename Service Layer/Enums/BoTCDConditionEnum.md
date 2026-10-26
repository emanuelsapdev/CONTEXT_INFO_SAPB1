# BoTCDConditionEnum — Condición de determinación de indicadores de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoTCDConditionEnum`
- **Descripción (ES):** Condición de determinación de indicadores de impuestos
- **Underlying type:** Edm.Int32
- **Members:** 22

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `tcdcNone` | 0 | None | Ninguna |
| `tcdcFederalTaxID` | 1 | Federal Tax ID | ID fiscal federal |
| `tcdcShipToAddress` | 2 | Ship To Address | Dirección de envío |
| `tcdcShipToStreePOBox` | 3 | Ship To Stree PO Box | Calle/apartado postal de envío |
| `tcdcShipToCity` | 4 | Ship To City | Ciudad de envío |
| `tcdcShipToZipCode` | 5 | Ship To Zip Code | Código postal de envío |
| `tcdcShipToCounty` | 6 | Ship To County | Condado de envío |
| `tcdcShipToState` | 7 | Ship To State | Estado de envío |
| `tcdcShipToCountry` | 8 | Ship To Country | País de envío |
| `tcdcItem` | 9 | Item | Artículo |
| `tcdcItemGroup` | 10 | Item Group | Grupo de artículos |
| `tcdcBusinessPartner` | 11 | Business Partner | Socio de negocios |
| `tcdcCustomerGroup` | 12 | Customer Group | Grupo de clientes |
| `tcdcVendorGroup` | 13 | Vendor Group | Grupo de proveedores |
| `tcdcWarehouse` | 14 | Warehouse | Almacén |
| `tcdcGLAccount` | 15 | G/L Account | Cuenta de mayor |
| `tcdcCustomerEquTax` | 16 | Customer Equ Tax | Recargo de equivalencia del cliente |
| `tcdcTaxStatus` | 17 | Tax Status | Estado fiscal |
| `tcdcFreight` | 18 | Freight | Gastos adicionales |
| `tcdcUDF` | 19 | UDF | Campo de usuario |
| `tcdcBranchNumber` | 20 | Branch Number | Número de sucursal |
| `tcdcTypeOfBusiness` | 21 | Type Of Business | Tipo de negocio |

## Used by (5 properties)

- [TaxCodeDetermination](../Entidades/TaxCodeDeterminations.md).`Condition1`
- [TaxCodeDetermination](../Entidades/TaxCodeDeterminations.md).`Condition2`
- [TaxCodeDetermination](../Entidades/TaxCodeDeterminations.md).`Condition3`
- [TaxCodeDetermination](../Entidades/TaxCodeDeterminations.md).`Condition4`
- [TaxCodeDetermination](../Entidades/TaxCodeDeterminations.md).`Condition5`
