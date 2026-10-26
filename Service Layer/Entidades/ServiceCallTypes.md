# ServiceCallTypes — Tipos de llamadas de servicio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ServiceCallTypes`
- **Descripción (ES):** Tipos de llamadas de servicio
- **Entity type:** `ServiceCallType`
- **Key:** `CallTypeID` (Edm.Int32)
- **DB tables (main / lines):** [OSCT](../../Tablas%20SAP%20B1/OSCT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ServiceCallTypes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ServiceCallTypes/$count` | Contar |
| Get by key | `GET /b1s/v2/ServiceCallTypes(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ServiceCallTypes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ServiceCallTypes(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ServiceCallTypes(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ServiceCallTypes(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CallTypeID` 🔑 | Edm.Int32 | No | Call Type ID | ID de tipo de llamada |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |
| 4 | `Active` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active | Activo |

## Navigation properties (1)

Use `GET /b1s/v2/ServiceCallTypes(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ServiceCalls` | Collection([ServiceCall](../Entidades/ServiceCalls.md)) | [ServiceCalls](ServiceCalls.md) |  | Llamadas de servicio |
