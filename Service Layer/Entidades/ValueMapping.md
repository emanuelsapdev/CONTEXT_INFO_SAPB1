# ValueMapping — Mapeo de valores

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ValueMapping`
- **Descripción (ES):** Mapeo de valores
- **Entity type:** `VM_B1ValuesData`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OMPO](../../Tablas%20SAP%20B1/OMPO.md), [MPO1](../../Tablas%20SAP%20B1/MPO1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ValueMapping?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ValueMapping/$count` | Contar |
| Get by key | `GET /b1s/v2/ValueMapping(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ValueMapping` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ValueMapping(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ValueMapping(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ValueMapping(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `ObjectId` | Edm.Int32 | Yes | Object ID | ID de objeto |
| 3 | `ObjectAbsEntry` | Edm.String | Yes | Object Abs Entry | Entrada absoluta del objeto |
| 4 | `VM_ThirdPartyValuesCollection` | Collection([VM_ThirdPartyValuesData](../Tipos-Complejos/VM_ThirdPartyValuesData.md)) | Yes | VM Third Party Values Collection | Colección de valores de terceros (mapeo de valores) |

## Service operations that use this type

- [`ValueMappingService_GetMappedB1Value`](../Servicios/ValueMappingService.md#valuemappingservice_getmappedb1value)
- [`ValueMappingService_GetThirdPartyValuesForB1Value`](../Servicios/ValueMappingService.md#valuemappingservice_getthirdpartyvaluesforb1value)
