# DeductibleTaxes — Impuestos deducibles

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `DeductibleTaxes`
- **Descripción (ES):** Impuestos deducibles
- **Entity type:** `DeductibleTax`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [ORTG](../../Tablas%20SAP%20B1/ORTG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/DeductibleTaxes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/DeductibleTaxes/$count` | Contar |
| Get by key | `GET /b1s/v2/DeductibleTaxes('value')` | Obtener por clave |
| Create | `POST /b1s/v2/DeductibleTaxes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/DeductibleTaxes('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/DeductibleTaxes('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/DeductibleTaxes('value')` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Inactive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inactive | Inactivo |
| 4 | `Category` | [BoVatCategoryEnum](../Enums/BoVatCategoryEnum.md) | Yes | Category | Categoría |
| 5 | `DeductibleTaxRate` | Edm.Double | Yes | Deductible Tax Rate | Tasa de impuesto deducible |
