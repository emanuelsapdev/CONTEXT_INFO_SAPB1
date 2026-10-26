# PMS_StageData — Subproyecto - Datos de etapa

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PMS_StageData`
- **Descripción (ES):** Subproyecto - Datos de etapa
- **Description (EN):** PMS Stage Data
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 30

## Properties (30)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineID` | Edm.Int32 | Yes | Line ID | ID de línea |
| 2 | `StageID` | Edm.Int32 | Yes | Stage ID | ID de etapa |
| 3 | `StageType` | Edm.Int32 | Yes | Stage Type | Tipo de etapa |
| 4 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 5 | `CloseDate` | Edm.DateTimeOffset | Yes | Close Date | Fecha de cierre |
| 6 | `Task` | Edm.Int32 | Yes | Task | Tarea |
| 7 | `Description` | Edm.String | Yes | Description | Descripción |
| 8 | `ExpectedCosts` | Edm.Double | Yes | Expected Costs | Costos previstos |
| 9 | `InvoicedAmountSales` | Edm.Double | Yes | Invoiced Amount Sales | Importe facturado (ventas) |
| 10 | `OpenAmountSales` | Edm.Double | Yes | Open Amount Sales | Importe abierto (ventas) |
| 11 | `InvoicedAmountPurchase` | Edm.Double | Yes | Invoiced Amount Purchase | Importe facturado (compras) |
| 12 | `OpenAmountPurchase` | Edm.Double | Yes | Open Amount Purchase | Importe abierto (compras) |
| 13 | `PercentualCompletness` | Edm.Double | Yes | Percentual Completness | Porcentaje de completitud |
| 14 | `IsFinished` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Finished | Está finalizado |
| 15 | `StageOwner` | Edm.Int32 | Yes | Stage Owner | Responsable de la etapa |
| 16 | `DependsOnStage1` | Edm.Int32 | Yes | Depends On Stage 1 | Depende de la etapa 1 |
| 17 | `DependsOnStage2` | Edm.Int32 | Yes | Depends On Stage 2 | Depende de la etapa 2 |
| 18 | `DependsOnStage3` | Edm.Int32 | Yes | Depends On Stage 3 | Depende de la etapa 3 |
| 19 | `DependsOnStage4` | Edm.Int32 | Yes | Depends On Stage 4 | Depende de la etapa 4 |
| 20 | `StageDependency1Type` | [StageDepTypeEnum](../Enums/StageDepTypeEnum.md) | Yes | Stage Dependency 1 Type | Tipo de dependencia de etapa 1 |
| 21 | `StageDependency2Type` | [StageDepTypeEnum](../Enums/StageDepTypeEnum.md) | Yes | Stage Dependency 2 Type | Tipo de dependencia de etapa 2 |
| 22 | `StageDependency3Type` | [StageDepTypeEnum](../Enums/StageDepTypeEnum.md) | Yes | Stage Dependency 3 Type | Tipo de dependencia de etapa 3 |
| 23 | `StageDependency4Type` | [StageDepTypeEnum](../Enums/StageDepTypeEnum.md) | Yes | Stage Dependency 4 Type | Tipo de dependencia de etapa 4 |
| 24 | `DependsOnStageID1` | Edm.Int32 | Yes | Depends On Stage ID 1 | Depende del ID de etapa 1 |
| 25 | `DependsOnStageID2` | Edm.Int32 | Yes | Depends On Stage ID 2 | Depende del ID de etapa 2 |
| 26 | `DependsOnStageID3` | Edm.Int32 | Yes | Depends On Stage ID 3 | Depende del ID de etapa 3 |
| 27 | `DependsOnStageID4` | Edm.Int32 | Yes | Depends On Stage ID 4 | Depende del ID de etapa 4 |
| 28 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 29 | `UniqueID` | Edm.String | Yes | Unique ID | ID único |
| 30 | `FinishedDate` | Edm.DateTimeOffset | Yes | Finished Date | Fecha de finalización |

## Used by (properties)

- [PM_SubprojectDocumentData](PM_SubprojectDocumentData.md).`PMS_StagesCollection`
