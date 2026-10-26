# TrackingNoteBroker — Agente de la nota de seguimiento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TrackingNoteBroker`
- **Descripción (ES):** Agente de la nota de seguimiento
- **Description (EN):** Tracking Note Broker

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TrackingNoteNumber` | Edm.Int32 | Yes | Tracking Note Number | Número de la nota de seguimiento |
| 2 | `TrackingNoteLineNumber` | Edm.Int32 | Yes | Tracking Note Line Number | Número de línea de la nota de seguimiento |
| 3 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 4 | `AgreementNumber` | Edm.Int32 | Yes | Agreement Number | Número de acuerdo |

## Used by (properties)

- [TrackingNote](../Entidades/TrackingNotes.md).`TrackingNoteBrokerCollection`
