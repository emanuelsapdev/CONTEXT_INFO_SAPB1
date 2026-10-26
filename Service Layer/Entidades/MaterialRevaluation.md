# MaterialRevaluation — Revalorización de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `MaterialRevaluation`
- **Descripción (ES):** Revalorización de inventario
- **Entity type:** `MaterialRevaluation` (open type: accepts dynamic/UDF properties)
- **Key:** `DocEntry` (Edm.Int32)
- **DB tables (main / lines):** [OMRV](../../Tablas%20SAP%20B1/OMRV.md), [MRV1](../../Tablas%20SAP%20B1/MRV1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 23 · **Navigation properties:** 3 · **Bound actions:** 2

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/MaterialRevaluation?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/MaterialRevaluation/$count` | Contar |
| Get by key | `GET /b1s/v2/MaterialRevaluation(1)` | Obtener por clave |
| Create | `POST /b1s/v2/MaterialRevaluation` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/MaterialRevaluation(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/MaterialRevaluation(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/MaterialRevaluation(1)` (only if the B1 object allows removal) | Borrar |
| Action `Cancel` | `POST /b1s/v2/MaterialRevaluation(1)/Cancel` | Cancelar |
| Action `Close` | `POST /b1s/v2/MaterialRevaluation(1)/Close` | Cerrar |

## Properties (23)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocNum` | Edm.Int32 | Yes | Document Number | Número de documento |
| 2 | `DocDate` | Edm.DateTimeOffset | Yes | Document Date | Fecha de contabilización del documento |
| 3 | `Reference1` | Edm.String | Yes | Reference 1 | Referencia 1 |
| 4 | `Reference2` | Edm.String | Yes | Reference 2 | Referencia 2 |
| 5 | `Comments` | Edm.String | Yes | Comments | Comentarios |
| 6 | `JournalMemo` | Edm.String | Yes | Journal Memo | Comentario del asiento |
| 7 | `DocTime` | Edm.TimeOfDay | Yes | Document Time | Hora del documento |
| 8 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 9 | `TaxDate` | Edm.DateTimeOffset | Yes | Tax Date | Fecha del documento (fecha de impuestos) |
| 10 | `DocEntry` 🔑 | Edm.Int32 | No | Document Entry | DocEntry (clave interna del documento) |
| 11 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 12 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 13 | `TransNum` | Edm.Int32 | Yes | Trans Number | Número de transacción |
| 14 | `RevalType` | Edm.String | Yes | Reval Type | Tipo de revalorización (precio/débito-crédito) |
| 15 | `RevaluationIncomeAccount` | Edm.String | Yes | Revaluation Income Account | Cuenta de ingresos por revalorización |
| 16 | `RevaluationExpenseAccount` | Edm.String | Yes | Revaluation Expense Account | Cuenta de gastos por revalorización |
| 17 | `DataSource` | Edm.String | Yes | Data Source | Origen de datos |
| 18 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 19 | `InflationRevaluation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inflation Revaluation | Revalorización por inflación |
| 20 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 21 | `CardName` | Edm.String | Yes | Card Name | Nombre del socio de negocios |
| 22 | `MaterialRevaluationLines` | Collection([MaterialRevaluationLine](../Tipos-Complejos/MaterialRevaluationLine.md)) | Yes | Material Revaluation Lines | Líneas de la revalorización de inventario |
| 23 | `MaterialRevaluationDocumentReferencesCollection` | Collection([MaterialRevaluationDocumentReferences](../Tipos-Complejos/MaterialRevaluationDocumentReferences.md)) | Yes | Material Revaluation Document References Collection | Referencias de documentos de la revalorización de inventario |

## Navigation properties (3)

Use `GET /b1s/v2/MaterialRevaluation(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `JournalEntry` | [JournalEntry](../Entidades/JournalEntries.md) | [JournalEntries](JournalEntries.md) | TransNum → JdtNum | Asientos contables |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | UserSignature → InternalKey | Usuario |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CardCode → CardCode | Socio de negocios |

## Bound actions (2)

### Cancel

- **Descripción (ES):** Cancelar
- **Request:** `POST /b1s/v2/MaterialRevaluation(1)/Cancel`

### Close

- **Descripción (ES):** Cerrar
- **Request:** `POST /b1s/v2/MaterialRevaluation(1)/Close`

