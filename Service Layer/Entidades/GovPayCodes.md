# GovPayCodes — Códigos de pago gubernamental

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `GovPayCodes`
- **Descripción (ES):** Códigos de pago gubernamental
- **Entity type:** `GovPayCode`
- **Key:** `AbsId` (Edm.Int32)
- **DB tables (main / lines):** [OGPC](../../Tablas%20SAP%20B1/OGPC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/GovPayCodes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/GovPayCodes/$count` | Contar |
| Get by key | `GET /b1s/v2/GovPayCodes(1)` | Obtener por clave |
| Create | `POST /b1s/v2/GovPayCodes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/GovPayCodes(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/GovPayCodes(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/GovPayCodes(1)` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsId` 🔑 | Edm.Int32 | No | Abs ID | ID absoluto |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Descr` | Edm.String | Yes | Description | Descripción |
| 4 | `StateTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | State Tax | Impuesto estatal |
| 5 | `Prdcity` | [GovPayCodePeriodicityEnum](../Enums/GovPayCodePeriodicityEnum.md) | Yes | Prdcity | Ciudad de producción |
| 6 | `GovPayCodeAuthorities` | Collection([GovPayCodeAuthority](../Tipos-Complejos/GovPayCodeAuthority.md)) | Yes | Gov Pay Code Authorities | Autoridades del código de pago gubernamental |

## Navigation properties (1)

Use `GET /b1s/v2/GovPayCodes(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `NFTaxCategories` | Collection([NFTaxCategory](../Entidades/NFTaxCategories.md)) | [NFTaxCategories](NFTaxCategories.md) |  | Categorías de impuestos de Nota Fiscal |
