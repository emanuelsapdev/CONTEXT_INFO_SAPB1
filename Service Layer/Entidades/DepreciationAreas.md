# DepreciationAreas — Áreas de amortización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `DepreciationAreas`
- **Descripción (ES):** Áreas de amortización
- **Entity type:** `DepreciationArea`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [ODPA](../../Tablas%20SAP%20B1/ODPA.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 13 · **Navigation properties:** 10 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/DepreciationAreas?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/DepreciationAreas/$count` | Contar |
| Get by key | `GET /b1s/v2/DepreciationAreas('value')` | Obtener por clave |
| Create | `POST /b1s/v2/DepreciationAreas` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/DepreciationAreas('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/DepreciationAreas('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/DepreciationAreas('value')` (only if the B1 object allows removal) | Borrar |

## Properties (13)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `PostingOfDepreciation` | [PostingOfDepreciationEnum](../Enums/PostingOfDepreciationEnum.md) | Yes | Posting Of Depreciation | Contabilización de la amortización |
| 4 | `RetirementMethod` | [RetirementMethodEnum](../Enums/RetirementMethodEnum.md) | Yes | Retirement Method | Método de baja |
| 5 | `AreaType` | [AreaTypeEnum](../Enums/AreaTypeEnum.md) | Yes | Area Type | Tipo de área |
| 6 | `DerivedArea` | Edm.String | Yes | Derived Area | Área derivada |
| 7 | `MainBookingArea` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Main Booking Area | Área de contabilización principal |
| 8 | `DirectRevenuePosting` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Direct Revenue Posting | Contabilización directa de ingresos |
| 9 | `TaxCreditControl` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tax Credit Control | Control de crédito fiscal |
| 10 | `TaxType` | Edm.Int32 | Yes | Tax Type | Tipo de impuesto |
| 11 | `BPForTaxCorrection` | Edm.String | Yes | Business Partner For Tax Correction | Socio de negocios para corrección de impuestos |
| 12 | `ItemForTaxCorrection` | Edm.String | Yes | Item For Tax Correction | Artículo para corrección de impuestos |
| 13 | `UsageForTaxCorrection` | Edm.Int32 | Yes | Usage For Tax Correction | Uso para corrección de impuestos |

## Navigation properties (10)

Use `GET /b1s/v2/DepreciationAreas('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `AssetRetirement` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetRetirement](AssetRetirement.md) |  | Baja de activos |
| `AssetTransfer` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetTransfer](AssetTransfer.md) |  | Transferencia de activos |
| `AssetRevaluations` | Collection([AssetRevaluation](../Entidades/AssetRevaluations.md)) | [AssetRevaluations](AssetRevaluations.md) |  | Revalorizaciones de activos |
| `AssetManualDepreciation` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetManualDepreciation](AssetManualDepreciation.md) |  | Amortización manual de activos |
| `AssetCapitalization` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetCapitalization](AssetCapitalization.md) |  | Capitalización de activos fijos |
| `AssetCapitalizationCreditMemo` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetCapitalizationCreditMemo](AssetCapitalizationCreditMemo.md) |  | Nota de crédito de capitalización de activos |
| `SalesTaxAuthoritiesType` | [SalesTaxAuthoritiesType](../Entidades/SalesTaxAuthoritiesTypes.md) | [SalesTaxAuthoritiesTypes](SalesTaxAuthoritiesTypes.md) | TaxType → Numerator | Tipos de autoridades del impuesto sobre ventas |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | BPForTaxCorrection → CardCode | Socio de negocios |
| `Item` | [Item](../Entidades/Items.md) | [Items](Items.md) | ItemForTaxCorrection → ItemCode | Artículos |
| `NotaFiscalUsage` | [NotaFiscalUsage](../Entidades/NotaFiscalUsage.md) | [NotaFiscalUsage](NotaFiscalUsage.md) | UsageForTaxCorrection → ID | Uso de Nota Fiscal |
