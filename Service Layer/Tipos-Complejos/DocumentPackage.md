# DocumentPackage — Paquetes del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocumentPackage`
- **Descripción (ES):** Paquetes del documento
- **Description (EN):** Document Package
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Number` | Edm.Int32 | Yes | Number | Número |
| 2 | `Type` | Edm.String | Yes | Type | Tipo |
| 3 | `TotalWeight` | Edm.Double | Yes | Total Weight | Peso total |
| 4 | `Units` | Edm.Int32 | Yes | Units | Unidades |
| 5 | `DocumentPackageItems` | Collection([DocumentPackageItem](../Tipos-Complejos/DocumentPackageItem.md)) | Yes | Document Package Items | Artículos de paquetes del documento |

## Used by (properties)

- [Document](../Entidades/PurchaseQuotations.md).`DocumentPackages`
