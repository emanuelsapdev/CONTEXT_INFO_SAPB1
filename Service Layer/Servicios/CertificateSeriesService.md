# CertificateSeriesService — Servicio de series de certificados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `CertificateSeriesService`
- **Descripción (ES):** Servicio de series de certificados
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`CertificateSeriesService_GetCertificateSeriesList`](#certificateseriesservice_getcertificateserieslist) | action | Collection([CertificateSeriesParams](../Tipos-Complejos/CertificateSeriesParams.md)) | Get Certificate Series List | Obtener lista de series de certificados |

## CertificateSeriesService_GetCertificateSeriesList

- **Descripción (ES):** Obtener lista de series de certificados
- **Request:** `POST /b1s/v2/CertificateSeriesService_GetCertificateSeriesList`
- **Parameters:** none
- **Returns:** Collection([CertificateSeriesParams](../Tipos-Complejos/CertificateSeriesParams.md))

