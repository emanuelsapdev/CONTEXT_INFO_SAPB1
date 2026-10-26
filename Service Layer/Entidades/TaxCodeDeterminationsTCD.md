# TaxCodeDeterminationsTCD — Determinación de indicadores de impuestos (TCD)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `TaxCodeDeterminationsTCD`
- **Descripción (ES):** Determinación de indicadores de impuestos (TCD)
- **Entity type:** `TaxCodeDeterminationTCD`
- **Key:** `AbsId` (Edm.Int32)
- **DB tables (main / lines):** [OTCD](../../Tablas%20SAP%20B1/OTCD.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 7 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/TaxCodeDeterminationsTCD?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/TaxCodeDeterminationsTCD/$count` | Contar |
| Get by key | `GET /b1s/v2/TaxCodeDeterminationsTCD(1)` | Obtener por clave |
| Create | `POST /b1s/v2/TaxCodeDeterminationsTCD` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/TaxCodeDeterminationsTCD(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/TaxCodeDeterminationsTCD(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/TaxCodeDeterminationsTCD(1)` (only if the B1 object allows removal) | Borrar |

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsId` 🔑 | Edm.Int32 | No | Abs ID | ID absoluto |
| 2 | `TcdType` | [TaxCodeDeterminationTCDTypeEnum](../Enums/TaxCodeDeterminationTCDTypeEnum.md) | Yes | Tcd Type | Tipo TCD |
| 3 | `DftArCode` | Edm.String | Yes | Default Ar Code | Código de ventas predeterminado |
| 4 | `DftApCode` | Edm.String | Yes | Default Ap Code | Código de compras predeterminado |
| 5 | `TaxCodeDeterminationTCDDefaultWTs` | Collection([TaxCodeDeterminationTCDDefaultWT](../Tipos-Complejos/TaxCodeDeterminationTCDDefaultWT.md)) | Yes | Tax Code Determination TCD Default W Ts | Retenciones predeterminadas de la determinación TCD |
| 6 | `TaxCodeDeterminationTCDByUsages` | Collection([TaxCodeDeterminationTCDByUsage](../Tipos-Complejos/TaxCodeDeterminationTCDByUsage.md)) | Yes | Tax Code Determination TCD By Usages | Determinación TCD por usos |
| 7 | `TaxCodeDeterminationTCDKeyFields` | Collection([TaxCodeDeterminationTCDKeyField](../Tipos-Complejos/TaxCodeDeterminationTCDKeyField.md)) | Yes | Tax Code Determination TCD Key Fields | Campos clave de la determinación TCD |
