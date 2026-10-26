# BPVatExemptions — Exenciones de IVA del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BPVatExemptions`
- **Descripción (ES):** Exenciones de IVA del socio de negocios
- **Entity type:** `BPVatExemptions`
- **Key:** `AbsoluteEntry` (Edm.Int32)
- **DB tables (main / lines):** [OVEB](../../Tablas%20SAP%20B1/OVEB.md), [VEB1](../../Tablas%20SAP%20B1/VEB1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BPVatExemptions?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BPVatExemptions/$count` | Contar |
| Get by key | `GET /b1s/v2/BPVatExemptions(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BPVatExemptions` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BPVatExemptions(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BPVatExemptions(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BPVatExemptions(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsoluteEntry` 🔑 | Edm.Int32 | No | Absolute Entry | Entrada absoluta (ID interno) |
| 2 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 3 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 4 | `BPVatExemptionsLines` | Collection([BPVatExemptionsLine](../Tipos-Complejos/BPVatExemptionsLine.md)) | Yes | Business Partner Vat Exemptions Lines | Líneas de exenciones de IVA del socio de negocios |

## Navigation properties (1)

Use `GET /b1s/v2/BPVatExemptions(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | BPCode → CardCode | Socio de negocios |
