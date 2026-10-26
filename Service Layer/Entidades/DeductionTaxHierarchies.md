# DeductionTaxHierarchies — Jerarquías de deducción de retenciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `DeductionTaxHierarchies`
- **Descripción (ES):** Jerarquías de deducción de retenciones
- **Entity type:** `DeductionTaxHierarchy` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [ODDT](../../Tablas%20SAP%20B1/ODDT.md), [DDT1](../../Tablas%20SAP%20B1/DDT1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 10 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/DeductionTaxHierarchies?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/DeductionTaxHierarchies/$count` | Contar |
| Get by key | `GET /b1s/v2/DeductionTaxHierarchies(1)` | Obtener por clave |
| Create | `POST /b1s/v2/DeductionTaxHierarchies` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/DeductionTaxHierarchies(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/DeductionTaxHierarchies(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/DeductionTaxHierarchies(1)` (only if the B1 object allows removal) | Borrar |

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 3 | `HierarchyCode` | Edm.String | Yes | Hierarchy Code | Código de jerarquía |
| 4 | `HierarchyName` | Edm.String | Yes | Hierarchy Name | Nombre de jerarquía |
| 5 | `ValidFrom` | Edm.DateTimeOffset | Yes | Valid From | Válido desde |
| 6 | `ValidUntil` | Edm.DateTimeOffset | Yes | Valid Until | Válido hasta |
| 7 | `DeductionPercent` | Edm.Double | Yes | Deduction Percent | Porcentaje de deducción |
| 8 | `MaximumTotal` | Edm.Double | Yes | Maximum Total | Total máximo |
| 9 | `LastUpdated` | Edm.DateTimeOffset | Yes | Last Updated | Última actualización |
| 10 | `DeductionTaxHierarchies_Lines` | Collection([DeductionTaxHierarchies_Line](../Tipos-Complejos/DeductionTaxHierarchies_Line.md)) | Yes | Deduction Tax Hierarchies Lines | Líneas de la jerarquía de deducción de retenciones |

## Navigation properties (1)

Use `GET /b1s/v2/DeductionTaxHierarchies(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | BPCode → CardCode | Socio de negocios |
