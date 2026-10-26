# BoReportLayoutItemTypeEnum — Tipo de elemento del formato de informe

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoReportLayoutItemTypeEnum`
- **Descripción (ES):** Tipo de elemento del formato de informe
- **Underlying type:** Edm.Int32
- **Members:** 10

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rlitPageHeader` | 0 | Page Header | Encabezado de página |
| `rlitStartOfReport` | 1 | Start Of Report | Inicio del informe |
| `rlitRepetitiveAreaHeader` | 2 | Repetitive Area Header | Encabezado del área repetitiva |
| `rlitRepetitiveArea` | 3 | Repetitive Area | Área repetitiva |
| `rlitRepetitiveAreaFooter` | 4 | Repetitive Area Footer | Pie del área repetitiva |
| `rlitEndOfReport` | 5 | End Of Report | Fin del informe |
| `rlitPageFooter` | 6 | Page Footer | Pie de página |
| `rlitTextField` | 7 | Text Field | Campo de texto |
| `rlitPictureField` | 8 | Picture Field | Campo de imagen |
| `rlitUserField` | 9 | User Field | Campo de usuario |

## Used by (1 properties)

- [ReportLayoutItem](../Tipos-Complejos/ReportLayoutItem.md).`Type`
