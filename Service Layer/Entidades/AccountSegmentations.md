# AccountSegmentations — Segmentaciones de cuentas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `AccountSegmentations`
- **Descripción (ES):** Segmentaciones de cuentas
- **Entity type:** `AccountSegmentation` (open type: accepts dynamic/UDF properties)
- **Key:** `Numerator` (Edm.Int32)
- **DB tables (main / lines):** [OASG](../../Tablas%20SAP%20B1/OASG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/AccountSegmentations?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/AccountSegmentations/$count` | Contar |
| Get by key | `GET /b1s/v2/AccountSegmentations(1)` | Obtener por clave |
| Create | `POST /b1s/v2/AccountSegmentations` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/AccountSegmentations(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/AccountSegmentations(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/AccountSegmentations(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Numerator` 🔑 | Edm.Int32 | No | Numerator | Numerador |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Size` | Edm.Int32 | Yes | Size | Tamaño |
| 4 | `Type` | [AccountSegmentationTypeEnum](../Enums/AccountSegmentationTypeEnum.md) | Yes | Type | Tipo |
| 5 | `AccountSegmentationsCategories` | Collection([AccountSegmentationsCategory](../Tipos-Complejos/AccountSegmentationsCategory.md)) | Yes | Account Segmentations Categories | Categorías de segmentación de cuentas |

## Navigation properties (1)

Use `GET /b1s/v2/AccountSegmentations(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `AccountSegmentationCategories` | Collection([AccountSegmentationCategory](../Entidades/AccountSegmentationCategories.md)) | [AccountSegmentationCategories](AccountSegmentationCategories.md) |  | Categorías de segmentación de cuentas |
