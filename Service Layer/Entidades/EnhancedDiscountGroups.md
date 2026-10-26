# EnhancedDiscountGroups — Grupos de descuento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `EnhancedDiscountGroups`
- **Descripción (ES):** Grupos de descuento
- **Entity type:** `EnhancedDiscountGroup`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OEDG](../../Tablas%20SAP%20B1/OEDG.md), [EDG1](../../Tablas%20SAP%20B1/EDG1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 8 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/EnhancedDiscountGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/EnhancedDiscountGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/EnhancedDiscountGroups(1)` | Obtener por clave |
| Create | `POST /b1s/v2/EnhancedDiscountGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/EnhancedDiscountGroups(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/EnhancedDiscountGroups(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/EnhancedDiscountGroups(1)` (only if the B1 object allows removal) | Borrar |

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Type` | [DiscountGroupTypeEnum](../Enums/DiscountGroupTypeEnum.md) | Yes | Type | Tipo |
| 3 | `ObjectCode` | Edm.String | Yes | Object Code | Código de objeto |
| 4 | `DiscountRelations` | [DiscountGroupRelationsEnum](../Enums/DiscountGroupRelationsEnum.md) | Yes | Discount Relations | Relaciones de descuento |
| 5 | `Active` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active | Activo |
| 6 | `ValidFrom` | Edm.DateTimeOffset | Yes | Valid From | Válido desde |
| 7 | `ValidTo` | Edm.DateTimeOffset | Yes | Valid To | Válido hasta |
| 8 | `DiscountGroupLineCollection` | Collection([DiscountGroupLine](../Tipos-Complejos/DiscountGroupLine.md)) | Yes | Discount Group Line Collection | Colección de líneas del grupo de descuento |
