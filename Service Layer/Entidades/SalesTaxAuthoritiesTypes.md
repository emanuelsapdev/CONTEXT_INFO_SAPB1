# SalesTaxAuthoritiesTypes — Tipos de autoridades del impuesto sobre ventas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SalesTaxAuthoritiesTypes`
- **Descripción (ES):** Tipos de autoridades del impuesto sobre ventas
- **Entity type:** `SalesTaxAuthoritiesType` (open type: accepts dynamic/UDF properties)
- **Key:** `Numerator` (Edm.Int32)
- **DB tables (main / lines):** [OSTT](../../Tablas%20SAP%20B1/OSTT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SalesTaxAuthoritiesTypes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SalesTaxAuthoritiesTypes/$count` | Contar |
| Get by key | `GET /b1s/v2/SalesTaxAuthoritiesTypes(1)` | Obtener por clave |
| Create | `POST /b1s/v2/SalesTaxAuthoritiesTypes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SalesTaxAuthoritiesTypes(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SalesTaxAuthoritiesTypes(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/SalesTaxAuthoritiesTypes(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `VAT` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | VAT | IVA |
| 4 | `Numerator` 🔑 | Edm.Int32 | No | Numerator | Numerador |
| 5 | `TaxCreditControl` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tax Credit Control | Control de crédito fiscal |

## Navigation properties (3)

Use `GET /b1s/v2/SalesTaxAuthoritiesTypes(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `SalesTaxAuthorities` | Collection([SalesTaxAuthority](../Entidades/SalesTaxAuthorities.md)) | [SalesTaxAuthorities](SalesTaxAuthorities.md) |  | Autoridades del impuesto sobre ventas |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | UserSignature → InternalKey | Usuario |
| `DepreciationAreas` | Collection([DepreciationArea](../Entidades/DepreciationAreas.md)) | [DepreciationAreas](DepreciationAreas.md) |  | Áreas de amortización |
