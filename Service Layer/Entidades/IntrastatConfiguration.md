# IntrastatConfiguration — Configuración de Intrastat

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `IntrastatConfiguration`
- **Descripción (ES):** Configuración de Intrastat
- **Entity type:** `IntrastatConfiguration`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 14 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/IntrastatConfiguration?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/IntrastatConfiguration/$count` | Contar |
| Get by key | `GET /b1s/v2/IntrastatConfiguration(1)` | Obtener por clave |
| Create | `POST /b1s/v2/IntrastatConfiguration` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/IntrastatConfiguration(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/IntrastatConfiguration(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/IntrastatConfiguration(1)` (only if the B1 object allows removal) | Borrar |

## Properties (14)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `ConfType` | [IntrastatConfigurationEnum](../Enums/IntrastatConfigurationEnum.md) | Yes | Conf Type | Tipo de configuración |
| 3 | `Code` | Edm.String | Yes | Code | Código |
| 4 | `Descr` | Edm.String | Yes | Description | Descripción |
| 5 | `PrcstVal` | Edm.Double | Yes | Prcst Val | Valor de costo |
| 6 | `SuppUnit` | Edm.Int32 | Yes | Supp Unit | Unidad suplementaria |
| 7 | `Export` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Export | Exportación |
| 8 | `Import` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Import | Importación |
| 9 | `StatCode` | Edm.String | Yes | Stat Code | Código estadístico |
| 10 | `DateFrom` | Edm.DateTimeOffset | Yes | Date From | Fecha desde |
| 11 | `DateTo` | Edm.DateTimeOffset | Yes | Date To | Fecha hasta |
| 12 | `Country` | Edm.String | Yes | Country | País |
| 13 | `ConfID` | Edm.String | Yes | Conf ID | ID de configuración |
| 14 | `TriangDeal` | [IntrastatConfigurationTriangDealEnum](../Enums/IntrastatConfigurationTriangDealEnum.md) | Yes | Triang Deal | Operación triangular |
