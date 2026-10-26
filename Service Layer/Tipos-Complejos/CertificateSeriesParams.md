# CertificateSeriesParams — Parámetros de series de certificados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CertificateSeriesParams`
- **Descripción (ES):** Parámetros de series de certificados
- **Description (EN):** Certificate Series Parameters

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Section` | Edm.Int32 | Yes | Section | Sección |
| 4 | `Location` | Edm.Int32 | Yes | Location | Ubicación |

## Used by (service operations)

- [`CertificateSeriesService_GetCertificateSeriesList`](../Servicios/CertificateSeriesService.md#certificateseriesservice_getcertificateserieslist)
