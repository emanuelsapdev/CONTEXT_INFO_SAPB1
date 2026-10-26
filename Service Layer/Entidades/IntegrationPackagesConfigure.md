# IntegrationPackagesConfigure — Configuración de paquetes de integración

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `IntegrationPackagesConfigure`
- **Descripción (ES):** Configuración de paquetes de integración
- **Entity type:** `IntegrationPackageConfigure`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/IntegrationPackagesConfigure?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/IntegrationPackagesConfigure/$count` | Contar |
| Get by key | `GET /b1s/v2/IntegrationPackagesConfigure(1)` | Obtener por clave |
| Create | `POST /b1s/v2/IntegrationPackagesConfigure` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/IntegrationPackagesConfigure(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/IntegrationPackagesConfigure(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/IntegrationPackagesConfigure(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Name` | Edm.String | Yes | Name | Nombre |
| 4 | `IsEnable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Enable | Está habilitado |
