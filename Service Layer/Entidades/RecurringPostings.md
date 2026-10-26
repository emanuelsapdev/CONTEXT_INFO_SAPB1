# RecurringPostings — Contabilizaciones periódicas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `RecurringPostings`
- **Descripción (ES):** Contabilizaciones periódicas
- **Entity type:** `RecurringPostings`
- **Key:** `Code` (Edm.String), `Instance` (Edm.Int32)
- **DB tables (main / lines):** [ORCR](../../Tablas%20SAP%20B1/ORCR.md), [RCR1](../../Tablas%20SAP%20B1/RCR1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 19 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/RecurringPostings?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/RecurringPostings/$count` | Contar |
| Get by key | `GET /b1s/v2/RecurringPostings(Code='value',Instance=1)` | Obtener por clave |
| Create | `POST /b1s/v2/RecurringPostings` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/RecurringPostings(Code='value',Instance=1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/RecurringPostings(Code='value',Instance=1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/RecurringPostings(Code='value',Instance=1)` (only if the B1 object allows removal) | Borrar |

## Properties (19)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `Instance` 🔑 | Edm.Int32 | No | Instance | Instancia |
| 4 | `Reference1` | Edm.String | Yes | Reference 1 | Referencia 1 |
| 5 | `Reference2` | Edm.String | Yes | Reference 2 | Referencia 2 |
| 6 | `Reference3` | Edm.String | Yes | Reference 3 | Referencia 3 |
| 7 | `TransactionCode` | Edm.String | Yes | Transaction Code | Código de transacción |
| 8 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 9 | `Frequency` | [BoFrequencyTypeEnum](../Enums/BoFrequencyTypeEnum.md) | Yes | Frequency | Frecuencia |
| 10 | `SubFrequency` | [BoSubFrequencyTypeEnum](../Enums/BoSubFrequencyTypeEnum.md) | Yes | Sub Frequency | Subfrecuencia |
| 11 | `NextExecution` | Edm.DateTimeOffset | Yes | Next Execution | Siguiente ejecución |
| 12 | `StampTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Stamp Tax | Impuesto de timbre |
| 13 | `AutomaticVAT` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Automatic VAT | IVA automático |
| 14 | `ManageWTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Manage W Tax | Gestionar retenciones |
| 15 | `DeferredTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Deferred Tax | Impuesto diferido |
| 16 | `ValidUntil` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Valid Until | Válido hasta |
| 17 | `ValidUntilDate` | Edm.DateTimeOffset | Yes | Valid Until Date | Fecha de validez hasta |
| 18 | `RecurringPostingsLineCollection` | Collection([RecurringPostingsLine](../Tipos-Complejos/RecurringPostingsLine.md)) | Yes | Recurring Postings Line Collection | Líneas de contabilizaciones periódicas |
| 19 | `RecurringPostingsDocumentReferenceCollection` | Collection([RecurringPostingsDocumentReference](../Tipos-Complejos/RecurringPostingsDocumentReference.md)) | Yes | Recurring Postings Document Reference Collection | Referencias de documentos de contabilizaciones periódicas |
