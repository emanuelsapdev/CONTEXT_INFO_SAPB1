# ImportOrExportTypeEnum — Tipo de importación/exportación (India)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ImportOrExportTypeEnum`
- **Descripción (ES):** Tipo de importación/exportación (India)
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `et_IpmortsOrExports` | 0 | Ipmorts Or Exports | Importaciones o exportaciones |
| `et_SEZ_Developer` | 1 | SEZ Developer | Desarrollador de ZEE |
| `et_SEZ_Unit` | 2 | SEZ Unit | Unidad de ZEE |
| `et_Deemed_ImportsOrExports` | 3 | Deemed Imports Or Exports | Importaciones/exportaciones consideradas |

## Used by (1 properties)

- [TaxExtension](../Tipos-Complejos/TaxExtension.md).`ImportOrExportType`
