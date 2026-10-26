# SalesOpportunities — Oportunidades de venta

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SalesOpportunities`
- **Descripción (ES):** Oportunidades de venta
- **Entity type:** `SalesOpportunities` (open type: accepts dynamic/UDF properties)
- **Key:** `SequentialNo` (Edm.Int32)
- **DB tables (main / lines):** [OOPR](../../Tablas%20SAP%20B1/OOPR.md), [OPR1](../../Tablas%20SAP%20B1/OPR1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 53 · **Navigation properties:** 11 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SalesOpportunities?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SalesOpportunities/$count` | Contar |
| Get by key | `GET /b1s/v2/SalesOpportunities(1)` | Obtener por clave |
| Create | `POST /b1s/v2/SalesOpportunities` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SalesOpportunities(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SalesOpportunities(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/SalesOpportunities(1)` (only if the B1 object allows removal) | Borrar |
| Action `Close` | `POST /b1s/v2/SalesOpportunities(1)/Close` | Cerrar |

## Properties (53)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `SequentialNo` 🔑 | Edm.Int32 | No | Sequential Number | Número secuencial |
| 2 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 3 | `SalesPerson` | Edm.Int32 | Yes | Sales Person | Empleado de ventas |
| 4 | `ContactPerson` | Edm.Int32 | Yes | Contact Person | Persona de contacto |
| 5 | `Source` | Edm.Int32 | Yes | Source | Origen |
| 6 | `InterestField1` | Edm.Int32 | Yes | Interest Field 1 | Campo de interés 1 |
| 7 | `InterestField2` | Edm.Int32 | Yes | Interest Field 2 | Campo de interés 2 |
| 8 | `InterestField3` | Edm.Int32 | Yes | Interest Field 3 | Campo de interés 3 |
| 9 | `InterestLevel` | Edm.Int32 | Yes | Interest Level | Nivel de interés |
| 10 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 11 | `PredictedClosingDate` | Edm.DateTimeOffset | Yes | Predicted Closing Date | Fecha de cierre prevista |
| 12 | `MaxLocalTotal` | Edm.Double | Yes | Max Local Total | Total máximo (moneda local) |
| 13 | `MaxSystemTotal` | Edm.Double | Yes | Max System Total | Total máximo (moneda del sistema) |
| 14 | `WeightedSumLC` | Edm.Double | Yes | Weighted Sum LC (local currency) | Importe ponderado (moneda local) |
| 15 | `WeightedSumSC` | Edm.Double | Yes | Weighted Sum SC (system currency) | Importe ponderado (moneda del sistema) |
| 16 | `GrossProfit` | Edm.Double | Yes | Gross Profit | Margen bruto |
| 17 | `GrossProfitTotalLocal` | Edm.Double | Yes | Gross Profit Total Local | Margen bruto total (moneda local) |
| 18 | `GrossProfitTotalSystem` | Edm.Double | Yes | Gross Profit Total System | Margen bruto total (moneda del sistema) |
| 19 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 20 | `Status` | [BoSoOsStatus](../Enums/BoSoOsStatus.md) | Yes | Status | Estado |
| 21 | `ReasonForClosing` | Edm.Int32 | Yes | Reason For Closing | Motivo del cierre |
| 22 | `TotalAmountLocal` | Edm.Double | Yes | Total Amount Local | Importe total (moneda local) |
| 23 | `TotalAmounSystem` | Edm.Double | Yes | Total Amoun System | Importe total (moneda del sistema) |
| 24 | `ClosingGrossProfitLocal` | Edm.Double | Yes | Closing Gross Profit Local | Margen bruto de cierre (moneda local) |
| 25 | `ClosingGrossProfitSystem` | Edm.Double | Yes | Closing Gross Profit System | Margen bruto de cierre (moneda del sistema) |
| 26 | `ClosingPercentage` | Edm.Double | Yes | Closing Percentage | Porcentaje de cierre |
| 27 | `CurrentStageNo` | Edm.Int32 | Yes | Current Stage Number | Número de etapa actual |
| 28 | `CurrentStageNumber` | Edm.Int32 | Yes | Current Stage Number | Número de etapa actual |
| 29 | `OpportunityName` | Edm.String | Yes | Opportunity Name | Nombre de la oportunidad |
| 30 | `Industry` | Edm.Int32 | Yes | Industry | Ramo (industria) |
| 31 | `LinkedDocumentType` | Edm.String | Yes | Linked Document Type | Tipo de documento vinculado |
| 32 | `DataOwnershipfield` | Edm.Int32 | Yes | Data Ownershipfield | Campo de propiedad de datos |
| 33 | `StatusRemarks` | Edm.String | Yes | Status Remarks | Comentarios del estado |
| 34 | `ProjectCode` | Edm.String | Yes | Project Code | Código de proyecto |
| 35 | `BPChanelName` | Edm.String | Yes | Business Partner Chanel Name | Nombre de socio de canal |
| 36 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 37 | `CustomerName` | Edm.String | Yes | Customer Name | Nombre del cliente |
| 38 | `DocumentCheckbox` | Edm.String | Yes | Document Checkbox | Casilla del documento |
| 39 | `LinkedDocumentNumber` | Edm.Int32 | Yes | Linked Document Number | Número de documento vinculado |
| 40 | `Territory` | Edm.Int32 | Yes | Territory | Territorio |
| 41 | `ClosingDate` | Edm.DateTimeOffset | Yes | Closing Date | Fecha de cierre |
| 42 | `BPChannelContact` | Edm.Int32 | Yes | Business Partner Channel Contact | Contacto del socio de canal |
| 43 | `BPChanelCode` | Edm.String | Yes | Business Partner Chanel Code | Código de socio de canal |
| 44 | `ClosingType` | [BoSoClosedInTypes](../Enums/BoSoClosedInTypes.md) | Yes | Closing Type | Tipo de cierre |
| 45 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 46 | `OpportunityType` | [OpportunityTypeEnum](../Enums/OpportunityTypeEnum.md) | Yes | Opportunity Type | Tipo de oportunidad |
| 47 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 48 | `UpdateTime` | Edm.TimeOfDay | Yes | Update Time | Hora de actualización |
| 49 | `SalesOpportunitiesLines` | Collection([SalesOpportunitiesLine](../Tipos-Complejos/SalesOpportunitiesLine.md)) | Yes | Sales Opportunities Lines | Líneas de la oportunidad de venta |
| 50 | `SalesOpportunitiesCompetition` | Collection([SalesOpportunitiesCompetitionItem](../Tipos-Complejos/SalesOpportunitiesCompetitionItem.md)) | Yes | Sales Opportunities Competition | Competencia de la oportunidad de venta |
| 51 | `SalesOpportunitiesPartners` | Collection([SalesOpportunitiesPartner](../Tipos-Complejos/SalesOpportunitiesPartner.md)) | Yes | Sales Opportunities Partners | Socios de la oportunidad de venta |
| 52 | `SalesOpportunitiesInterests` | Collection([SalesOpportunitiesInterest](../Tipos-Complejos/SalesOpportunitiesInterest.md)) | Yes | Sales Opportunities Interests | Intereses de la oportunidad de venta |
| 53 | `SalesOpportunitiesReasons` | Collection([SalesOpportunitiesReason](../Tipos-Complejos/SalesOpportunitiesReason.md)) | Yes | Sales Opportunities Reasons | Motivos de la oportunidad de venta |

## Navigation properties (11)

Use `GET /b1s/v2/SalesOpportunities(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CardCode → CardCode | Socio de negocios |
| `SalesPerson2` | [SalesPerson](../Entidades/SalesPersons.md) | [SalesPersons](SalesPersons.md) | SalesPerson → SalesEmployeeCode | Empleados del departamento de ventas |
| `SalesOpportunitySourceSetup` | [SalesOpportunitySourceSetup](../Entidades/SalesOpportunitySourcesSetup.md) | [SalesOpportunitySourcesSetup](SalesOpportunitySourcesSetup.md) | Source → SequenceNo | Configuración de fuentes de información de oportunidades |
| `SalesOpportunityInterestSetup` | [SalesOpportunityInterestSetup](../Entidades/SalesOpportunityInterestsSetup.md) | [SalesOpportunityInterestsSetup](SalesOpportunityInterestsSetup.md) | InterestField1 → SequenceNo | Configuración de intereses de oportunidades |
| `SalesOpportunityReasonSetup` | [SalesOpportunityReasonSetup](../Entidades/SalesOpportunityReasonsSetup.md) | [SalesOpportunityReasonsSetup](SalesOpportunityReasonsSetup.md) | ReasonForClosing → SequenceNo | Configuración de motivos de oportunidades |
| `SalesStage` | [SalesStage](../Entidades/SalesStages.md) | [SalesStages](SalesStages.md) | CurrentStageNo → SequenceNo | Etapas de venta |
| `Industry2` | [Industry](../Entidades/Industries.md) | [Industries](Industries.md) | Industry → IndustryCode | Ramos (industrias) |
| `EmployeeInfo` | [EmployeeInfo](../Entidades/EmployeesInfo.md) | [EmployeesInfo](EmployeesInfo.md) | DataOwnershipfield → EmployeeID | Empleados |
| `Project` | [Project](../Entidades/Projects.md) | [Projects](Projects.md) | ProjectCode → Code | Proyecto |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | UserSignature → InternalKey | Usuario |
| `Territory2` | [Territory](../Entidades/Territories.md) | [Territories](Territories.md) | Territory → TerritoryID | Territorios |

## Bound actions (1)

### Close

- **Descripción (ES):** Cerrar
- **Request:** `POST /b1s/v2/SalesOpportunities(1)/Close`

