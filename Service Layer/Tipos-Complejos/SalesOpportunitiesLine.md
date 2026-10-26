# SalesOpportunitiesLine — Líneas de la oportunidad de venta

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SalesOpportunitiesLine`
- **Descripción (ES):** Líneas de la oportunidad de venta
- **Description (EN):** Sales Opportunities Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 22

## Properties (22)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `SalesPerson` | Edm.Int32 | Yes | Sales Person | Empleado de ventas |
| 3 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 4 | `ClosingDate` | Edm.DateTimeOffset | Yes | Closing Date | Fecha de cierre |
| 5 | `StageKey` | Edm.Int32 | Yes | Stage Key | Clave de etapa |
| 6 | `PercentageRate` | Edm.Double | Yes | Percentage Rate | Tasa porcentual |
| 7 | `MaxLocalTotal` | Edm.Double | Yes | Max Local Total | Total máximo (moneda local) |
| 8 | `MaxSystemTotal` | Edm.Double | Yes | Max System Total | Total máximo (moneda del sistema) |
| 9 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 10 | `Contact` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Contact | Contacto |
| 11 | `Status` | [BoSoStatus](../Enums/BoSoStatus.md) | Yes | Status | Estado |
| 12 | `WeightedAmountLocal` | Edm.Double | Yes | Weighted Amount Local | Importe ponderado (moneda local) |
| 13 | `WeightedAmountSystem` | Edm.Double | Yes | Weighted Amount System | Importe ponderado (moneda del sistema) |
| 14 | `DocumentNumber` | Edm.Int32 | Yes | Document Number | Número de documento |
| 15 | `DocumentType` | [BoAPARDocumentTypes](../Enums/BoAPARDocumentTypes.md) | Yes | Document Type | Tipo de documento |
| 16 | `DocumentCheckbox` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Document Checkbox | Casilla del documento |
| 17 | `ContactPerson` | Edm.Int32 | Yes | Contact Person | Persona de contacto |
| 18 | `BPChanelName` | Edm.String | Yes | Business Partner Chanel Name | Nombre de socio de canal |
| 19 | `BPChanelCode` | Edm.String | Yes | Business Partner Chanel Code | Código de socio de canal |
| 20 | `SequenceNo` | Edm.Int32 | Yes | Sequence Number | Número de secuencia |
| 21 | `DataOwnershipfield` | Edm.Int32 | Yes | Data Ownershipfield | Campo de propiedad de datos |
| 22 | `BPChannelContact` | Edm.Int32 | Yes | Business Partner Channel Contact | Contacto del socio de canal |

## Used by (properties)

- [SalesOpportunities](../Entidades/SalesOpportunities.md).`SalesOpportunitiesLines`
