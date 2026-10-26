# DepreciationTypes — Tipos de amortización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `DepreciationTypes`
- **Descripción (ES):** Tipos de amortización
- **Entity type:** `DepreciationType`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [ODTP](../../Tablas%20SAP%20B1/ODTP.md), [DTP1](../../Tablas%20SAP%20B1/DTP1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 44 · **Navigation properties:** 6 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/DepreciationTypes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/DepreciationTypes/$count` | Contar |
| Get by key | `GET /b1s/v2/DepreciationTypes('value')` | Obtener por clave |
| Create | `POST /b1s/v2/DepreciationTypes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/DepreciationTypes('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/DepreciationTypes('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/DepreciationTypes('value')` (only if the B1 object allows removal) | Borrar |

## Properties (44)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `DepreciationMethod` | [DepreciationMethodEnum](../Enums/DepreciationMethodEnum.md) | Yes | Depreciation Method | Método de amortización |
| 4 | `MinimumDepreciatedValue` | Edm.Double | Yes | Minimum Depreciated Value | Valor amortizado mínimo |
| 5 | `RoundYearEndBookValue` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Round Year End Book Value | Redondear valor contable de fin de año |
| 6 | `IncludeSalvageInDepreciation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Salvage In Depreciation | Incluir valor residual en la amortización |
| 7 | `SalvagePercentage` | Edm.Double | Yes | Salvage Percentage | Porcentaje de valor residual |
| 8 | `AcquisitionPeriodControl` | [AcquisitionPeriodControlEnum](../Enums/AcquisitionPeriodControlEnum.md) | Yes | Acquisition Period Control | Control de período de adquisición |
| 9 | `SubsequentAcquisitionPeriodControl` | [SubsequentAcquisitionPeriodControlEnum](../Enums/SubsequentAcquisitionPeriodControlEnum.md) | Yes | Subsequent Acquisition Period Control | Control de período de adquisición posterior |
| 10 | `RetirementPeriodControl` | [RetirementPeriodControlEnum](../Enums/RetirementPeriodControlEnum.md) | Yes | Retirement Period Control | Control de período de baja |
| 11 | `AcquisitionProRataType` | [AcquisitionProRataTypeEnum](../Enums/AcquisitionProRataTypeEnum.md) | Yes | Acquisition Pro Rata Type | Tipo de prorrata de adquisición |
| 12 | `SubsequentAcquisitionProRataType` | [SubsequentAcquisitionProRataTypeEnum](../Enums/SubsequentAcquisitionProRataTypeEnum.md) | Yes | Subsequent Acquisition Pro Rata Type | Tipo de prorrata de adquisición posterior |
| 13 | `RetirementProRataType` | [RetirementProRataTypeEnum](../Enums/RetirementProRataTypeEnum.md) | Yes | Retirement Pro Rata Type | Tipo de prorrata de baja |
| 14 | `PercentageOfDepreciationReversedInRetirementYear` | Edm.Double | Yes | Percentage Of Depreciation Reversed In Retirement Year | Porcentaje de amortización revertido en el año de baja |
| 15 | `ValidFrom` | Edm.DateTimeOffset | Yes | Valid From | Válido desde |
| 16 | `ValidTo` | Edm.DateTimeOffset | Yes | Valid To | Válido hasta |
| 17 | `StraightLineCalculationMethod` | [StraightLineCalculationMethodEnum](../Enums/StraightLineCalculationMethodEnum.md) | Yes | Straight Line Calculation Method | Método de cálculo lineal |
| 18 | `StraightLinePercentage` | Edm.Double | Yes | Straight Line Percentage | Porcentaje lineal |
| 19 | `StraightLinePeriodControlDepreciationPeriods` | [StraightLinePeriodControlDepreciationPeriodsEnum](../Enums/StraightLinePeriodControlDepreciationPeriodsEnum.md) | Yes | Straight Line Period Control Depreciation Periods | Períodos de amortización lineal con control de período |
| 20 | `StraightLinePeriodControlFactor` | Edm.Double | Yes | Straight Line Period Control Factor | Factor lineal con control de período |
| 21 | `DecliningPercentage` | Edm.Double | Yes | Declining Percentage | Porcentaje decreciente |
| 22 | `DecliningFactor` | Edm.Double | Yes | Declining Factor | Factor decreciente |
| 23 | `DecliningChangeTo` | Edm.String | Yes | Declining Change To | Cambio decreciente a |
| 24 | `SpecialDepreciationCalculationMethod` | [SpecialDepreciationCalculationMethodEnum](../Enums/SpecialDepreciationCalculationMethodEnum.md) | Yes | Special Depreciation Calculation Method | Método de cálculo de amortización especial |
| 25 | `SpecialDepreciationConcessionPeriodYears` | Edm.Int32 | Yes | Special Depreciation Concession Period Years | Años del período de concesión de amortización especial |
| 26 | `SpecialDepreciationMaximumPercentage` | Edm.Double | Yes | Special Depreciation Maximum Percentage | Porcentaje máximo de amortización especial |
| 27 | `SpecialDepreciationNormalDepreciation` | Edm.String | Yes | Special Depreciation Normal Depreciation | Amortización especial - amortización normal |
| 28 | `SpecialDepreciationAlternativeDepreciation` | Edm.String | Yes | Special Depreciation Alternative Depreciation | Amortización especial - amortización alternativa |
| 29 | `DepreciationTypePool` | Edm.String | Yes | Depreciation Type Pool | Grupo de tipos de amortización |
| 30 | `ManualDepreciationReduceDepreciationBase` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Manual Depreciation Reduce Depreciation Base | Amortización manual reduce la base de amortización |
| 31 | `SpecialDepreciationMaximumAmount` | Edm.Double | Yes | Special Depreciation Maximum Amount | Importe máximo de amortización especial |
| 32 | `SpecialDepreciationMaximumFlag` | [SpecialDepreciationMaximumFlagEnum](../Enums/SpecialDepreciationMaximumFlagEnum.md) | Yes | Special Depreciation Maximum Flag | Indicador de máximo de amortización especial |
| 33 | `CalculationBase` | [CalculationBaseEnum](../Enums/CalculationBaseEnum.md) | Yes | Calculation Base | Base de cálculo |
| 34 | `DepreciationEndAtLastFullYear` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Depreciation End At Last Full Year | Fin de amortización en el último año completo |
| 35 | `IncludePreviousDepreciationInCapitalizationPeriod` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Previous Depreciation In Capitalization Period | Incluir amortización previa en el período de capitalización |
| 36 | `DeltaCoefficient` | Edm.Int32 | Yes | Delta Coefficient | Coeficiente delta |
| 37 | `MaximumDepreciableValue` | Edm.Double | Yes | Maximum Depreciable Value | Valor amortizable máximo |
| 38 | `FactorOnlyRelevantToFirstFiscalYear` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Factor Only Relevant To First Fiscal Year | Factor relevante solo para el primer ejercicio |
| 39 | `TransferSourcePeriodControl` | [TransferSourcePeriodControlEnum](../Enums/TransferSourcePeriodControlEnum.md) | Yes | Transfer Source Period Control | Control de período del origen de transferencia |
| 40 | `TransferTargetPeriodControl` | [TransferTargetPeriodControlEnum](../Enums/TransferTargetPeriodControlEnum.md) | Yes | Transfer Target Period Control | Control de período del destino de transferencia |
| 41 | `TransferSourceProRataType` | [TransferSourceProRataTypeEnum](../Enums/TransferSourceProRataTypeEnum.md) | Yes | Transfer Source Pro Rata Type | Tipo de prorrata del origen de transferencia |
| 42 | `TransferTargetProRataType` | [TransferTargetProRataTypeEnum](../Enums/TransferTargetProRataTypeEnum.md) | Yes | Transfer Target Pro Rata Type | Tipo de prorrata del destino de transferencia |
| 43 | `RoundingMethod` | [DepreciationRoundingMethodEnum](../Enums/DepreciationRoundingMethodEnum.md) | Yes | Rounding Method | Método de redondeo |
| 44 | `DepreciationLevelCollection` | Collection([DepreciationLevel](../Tipos-Complejos/DepreciationLevel.md)) | Yes | Depreciation Level Collection | Colección de niveles de amortización |

## Navigation properties (6)

Use `GET /b1s/v2/DepreciationTypes('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `AssetRetirement` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetRetirement](AssetRetirement.md) |  | Baja de activos |
| `AssetTransfer` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetTransfer](AssetTransfer.md) |  | Transferencia de activos |
| `AssetManualDepreciation` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetManualDepreciation](AssetManualDepreciation.md) |  | Amortización manual de activos |
| `AssetCapitalization` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetCapitalization](AssetCapitalization.md) |  | Capitalización de activos fijos |
| `DepreciationTypePool2` | [DepreciationTypePool](../Entidades/DepreciationTypePools.md) | [DepreciationTypePools](DepreciationTypePools.md) | DepreciationTypePool → Code | Grupos de tipos de amortización |
| `AssetCapitalizationCreditMemo` | Collection([AssetDocument](../Entidades/AssetRetirement.md)) | [AssetCapitalizationCreditMemo](AssetCapitalizationCreditMemo.md) |  | Nota de crédito de capitalización de activos |
