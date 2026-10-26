# NotaFiscalUsage — Uso de Nota Fiscal

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `NotaFiscalUsage`
- **Descripción (ES):** Uso de Nota Fiscal
- **Entity type:** `NotaFiscalUsage` (open type: accepts dynamic/UDF properties)
- **Key:** `ID` (Edm.Int32)
- **DB tables (main / lines):** [OUSG](../../Tablas%20SAP%20B1/OUSG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 9 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/NotaFiscalUsage?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/NotaFiscalUsage/$count` | Contar |
| Get by key | `GET /b1s/v2/NotaFiscalUsage(1)` | Obtener por clave |
| Create | `POST /b1s/v2/NotaFiscalUsage` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/NotaFiscalUsage(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/NotaFiscalUsage(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/NotaFiscalUsage(1)` (only if the B1 object allows removal) | Borrar |

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ID` 🔑 | Edm.Int32 | No | ID | ID |
| 2 | `Usage` | Edm.String | Yes | Usage | Uso |
| 3 | `IncomingInStateCFOPCode` | Edm.String | Yes | Incoming In State CFOP Code | Código CFOP entrante dentro del estado |
| 4 | `IncomingOutStateCFOPCode` | Edm.String | Yes | Incoming Out State CFOP Code | Código CFOP entrante fuera del estado |
| 5 | `IncomingImportCFOPCode` | Edm.String | Yes | Incoming Import CFOP Code | Código CFOP de importación entrante |
| 6 | `OutgoingInStateCFOPCode` | Edm.String | Yes | Outgoing In State CFOP Code | Código CFOP saliente dentro del estado |
| 7 | `OutgoingOutStateCFOPCode` | Edm.String | Yes | Outgoing Out State CFOP Code | Código CFOP saliente fuera del estado |
| 8 | `OutgoingExportCFOPCode` | Edm.String | Yes | Outgoing Export CFOP Code | Código CFOP de exportación saliente |
| 9 | `Description` | Edm.String | Yes | Description | Descripción |

## Navigation properties (3)

Use `GET /b1s/v2/NotaFiscalUsage(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `GLAccountAdvancedRules` | Collection([GLAccountAdvancedRule](../Entidades/GLAccountAdvancedRules.md)) | [GLAccountAdvancedRules](GLAccountAdvancedRules.md) |  | Reglas avanzadas de cuentas de mayor |
| `DepreciationAreas` | Collection([DepreciationArea](../Entidades/DepreciationAreas.md)) | [DepreciationAreas](DepreciationAreas.md) |  | Áreas de amortización |
| `NotaFiscalCFOP` | [NotaFiscalCFOP](../Entidades/NotaFiscalCFOP.md) | [NotaFiscalCFOP](NotaFiscalCFOP.md) | IncomingInStateCFOPCode → ID | CFOP de Nota Fiscal |
