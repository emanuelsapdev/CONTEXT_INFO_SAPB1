# BPFiscalRegistryID — ID de registro fiscal del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BPFiscalRegistryID`
- **Descripción (ES):** ID de registro fiscal del socio de negocios
- **Entity type:** `BPFiscalRegistryID` (open type: accepts dynamic/UDF properties)
- **Key:** `Numerator` (Edm.Int32)
- **DB tables (main / lines):** [CRD7](../../Tablas%20SAP%20B1/CRD7.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BPFiscalRegistryID?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BPFiscalRegistryID/$count` | Contar |
| Get by key | `GET /b1s/v2/BPFiscalRegistryID(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BPFiscalRegistryID` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BPFiscalRegistryID(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BPFiscalRegistryID(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BPFiscalRegistryID(1)` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Numerator` 🔑 | Edm.Int32 | No | Numerator | Numerador |
| 2 | `CNAECode` | Edm.String | Yes | CNAE Code | Código CNAE |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |

## Navigation properties (1)

Use `GET /b1s/v2/BPFiscalRegistryID(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPlaces` | Collection([BusinessPlace](../Entidades/BusinessPlaces.md)) | [BusinessPlaces](BusinessPlaces.md) |  | Lugares de negocios |
