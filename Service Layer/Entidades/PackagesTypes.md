# PackagesTypes — Tipos de paquete

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `PackagesTypes`
- **Descripción (ES):** Tipos de paquete
- **Entity type:** `PackagesType` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [OPKG](../../Tablas%20SAP%20B1/OPKG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 20 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/PackagesTypes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/PackagesTypes/$count` | Contar |
| Get by key | `GET /b1s/v2/PackagesTypes(1)` | Obtener por clave |
| Create | `POST /b1s/v2/PackagesTypes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/PackagesTypes(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/PackagesTypes(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/PackagesTypes(1)` (only if the B1 object allows removal) | Borrar |

## Properties (20)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Type` | Edm.String | Yes | Type | Tipo |
| 2 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 3 | `Length1` | Edm.Double | Yes | Length 1 | Longitud 1 |
| 4 | `Length1Unit` | Edm.Int32 | Yes | Length 1 Unit | Unidad de longitud 1 |
| 5 | `Length2` | Edm.Double | Yes | Length 2 | Longitud 2 |
| 6 | `Length2Unit` | Edm.Int32 | Yes | Length 2 Unit | Unidad de longitud 2 |
| 7 | `Width1` | Edm.Double | Yes | Width 1 | Ancho 1 |
| 8 | `Width1Unit` | Edm.Int32 | Yes | Width 1 Unit | Unidad de ancho 1 |
| 9 | `Width2` | Edm.Double | Yes | Width 2 | Ancho 2 |
| 10 | `Width2Unit` | Edm.Int32 | Yes | Width 2 Unit | Unidad de ancho 2 |
| 11 | `Height1` | Edm.Double | Yes | Height 1 | Altura 1 |
| 12 | `Height1Unit` | Edm.Int32 | Yes | Height 1 Unit | Unidad de altura 1 |
| 13 | `Height2` | Edm.Double | Yes | Height 2 | Altura 2 |
| 14 | `Height2Unit` | Edm.Int32 | Yes | Height 2 Unit | Unidad de altura 2 |
| 15 | `Volume` | Edm.Double | Yes | Volume | Volumen |
| 16 | `VolumeUnit` | Edm.Int32 | Yes | Volume Unit | Unidad de volumen |
| 17 | `Weight1` | Edm.Double | Yes | Weight 1 | Peso 1 |
| 18 | `Weight1Unit` | Edm.Int32 | Yes | Weight 1 Unit | Unidad de peso 1 |
| 19 | `Weight2` | Edm.Double | Yes | Weight 2 | Peso 2 |
| 20 | `Weight2Unit` | Edm.Int32 | Yes | Weight 2 Unit | Unidad de peso 2 |
