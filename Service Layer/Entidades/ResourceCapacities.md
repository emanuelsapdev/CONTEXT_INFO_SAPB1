# ResourceCapacities — Capacidades de recursos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ResourceCapacities`
- **Descripción (ES):** Capacidades de recursos
- **Entity type:** `ResourceCapacity`
- **Key:** `Id` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 24 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ResourceCapacities?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ResourceCapacities/$count` | Contar |
| Get by key | `GET /b1s/v2/ResourceCapacities(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ResourceCapacities` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ResourceCapacities(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ResourceCapacities(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ResourceCapacities(1)` (only if the B1 object allows removal) | Borrar |

## Properties (24)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Id` 🔑 | Edm.Int32 | No | ID | ID |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |
| 4 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 5 | `Type` | [ResourceCapacityTypeEnum](../Enums/ResourceCapacityTypeEnum.md) | Yes | Type | Tipo |
| 6 | `Capacity` | Edm.Double | Yes | Capacity | Capacidad |
| 7 | `SourceType` | [ResourceCapacitySourceTypeEnum](../Enums/ResourceCapacitySourceTypeEnum.md) | Yes | Source Type | Tipo de origen |
| 8 | `SourceEntry` | Edm.Int32 | Yes | Source Entry | Entrada de origen |
| 9 | `SourceLineNum` | Edm.Int32 | Yes | Source Line Number | Línea de origen |
| 10 | `BaseType` | [ResourceCapacityBaseTypeEnum](../Enums/ResourceCapacityBaseTypeEnum.md) | Yes | Base Type | Tipo base (tipo de objeto del documento base) |
| 11 | `BaseEntry` | Edm.Int32 | Yes | Base Entry | Entrada base (DocEntry del documento base) |
| 12 | `BaseLineNum` | Edm.Int32 | Yes | Base Line Number | Número de línea base |
| 13 | `Action` | [ResourceCapacityActionEnum](../Enums/ResourceCapacityActionEnum.md) | Yes | Action | Acción |
| 14 | `OwningType` | [ResourceCapacityOwningTypeEnum](../Enums/ResourceCapacityOwningTypeEnum.md) | Yes | Owning Type | Tipo propietario |
| 15 | `OwningEntry` | Edm.Int32 | Yes | Owning Entry | Entrada propietaria |
| 16 | `OwningLineNum` | Edm.Int32 | Yes | Owning Line Number | Número de línea propietaria |
| 17 | `RevertedType` | [ResourceCapacityRevertedTypeEnum](../Enums/ResourceCapacityRevertedTypeEnum.md) | Yes | Reverted Type | Tipo revertido |
| 18 | `RevertedEntry` | Edm.Int32 | Yes | Reverted Entry | Entrada revertida |
| 19 | `RevertedLineNum` | Edm.Int32 | Yes | Reverted Line Number | Línea revertida |
| 20 | `MemoSource` | [ResourceCapacityMemoSourceEnum](../Enums/ResourceCapacityMemoSourceEnum.md) | Yes | Memo Source | Origen del comentario |
| 21 | `Memo` | Edm.String | Yes | Memo | Comentario |
| 22 | `SingleRunCapacity` | Edm.Double | Yes | Single Run Capacity | Capacidad de ejecución única |
| 23 | `SingleRunMemoSource` | [ResourceCapacityMemoSourceEnum](../Enums/ResourceCapacityMemoSourceEnum.md) | Yes | Single Run Memo Source | Origen del comentario de ejecución única |
| 24 | `SingleRunMemo` | Edm.String | Yes | Single Run Memo | Comentario de ejecución única |

## Navigation properties (2)

Use `GET /b1s/v2/ResourceCapacities(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Resource` | [Resource](../Entidades/Resources.md) | [Resources](Resources.md) | Code → Code | Recursos |
| `Warehouse2` | [Warehouse](../Entidades/Warehouses.md) | [Warehouses](Warehouses.md) | Warehouse → WarehouseCode | Almacenes |
