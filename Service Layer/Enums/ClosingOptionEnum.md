# ClosingOptionEnum — Opción de cierre

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ClosingOptionEnum`
- **Descripción (ES):** Opción de cierre
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `coByCurrentSystemDate` | 1 | By Current System Date | Por fecha actual del sistema |
| `coByOriginalDocumentDate` | 2 | By Original Document Date | Por fecha del documento original |
| `coBySpecifiedDate` | 3 | By Specified Date | Por fecha especificada |

## Used by (4 properties)

- [AssetDocument](../Entidades/AssetRetirement.md).`CancellationOption`
- [AssetDocumentParams](../Tipos-Complejos/AssetDocumentParams.md).`CancellationOption`
- [Document](../Entidades/PurchaseQuotations.md).`ClosingOption`
- [DocumentCloseParams](../Tipos-Complejos/DocumentCloseParams.md).`ClosingOption`
