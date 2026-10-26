# PriceProceedMethodEnum — Método de procesamiento de precios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `PriceProceedMethodEnum`
- **Descripción (ES):** Método de procesamiento de precios
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ppmRemove` | 0 | Remove | Eliminar |
| `ppmUpdate` | 1 | Update | Actualizar |
| `ppmKeepCorresponding` | 2 | Keep Corresponding | Mantener los correspondientes |
| `ppmKeepAll` | 3 | Keep All | Mantener todos |

## Used by (1 properties)

- [AdminInfo](../Tipos-Complejos/AdminInfo.md).`PriceProceedMethod`
