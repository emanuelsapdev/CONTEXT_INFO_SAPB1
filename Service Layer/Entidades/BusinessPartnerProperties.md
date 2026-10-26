# BusinessPartnerProperties — Propiedades de socios de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BusinessPartnerProperties`
- **Descripción (ES):** Propiedades de socios de negocios
- **Entity type:** `BusinessPartnerProperty` (open type: accepts dynamic/UDF properties)
- **Key:** `PropertyCode` (Edm.Int32)
- **DB tables (main / lines):** [OCQG](../../Tablas%20SAP%20B1/OCQG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BusinessPartnerProperties?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BusinessPartnerProperties/$count` | Contar |
| Get by key | `GET /b1s/v2/BusinessPartnerProperties(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BusinessPartnerProperties` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BusinessPartnerProperties(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BusinessPartnerProperties(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BusinessPartnerProperties(1)` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PropertyCode` 🔑 | Edm.Int32 | No | Property Code | Código de propiedad |
| 2 | `PropertyName` | Edm.String | Yes | Property Name | Nombre de propiedad |
