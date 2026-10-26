# ExportDeterminationParams — Parámetros de determinaciones de exportación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ExportDeterminationParams`
- **Descripción (ES):** Parámetros de determinaciones de exportación
- **Description (EN):** Export Determination Parameters
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Code` | [ElectronicDocProtocolCodeStrEnum](../Enums/ElectronicDocProtocolCodeStrEnum.md) | Yes | Code | Código |
| 3 | `BusinessPartner` | Edm.String | Yes | Business Partner | Socio de negocios |
| 4 | `Country` | Edm.String | Yes | Country | País |
| 5 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 6 | `DocumentType` | Edm.String | Yes | Document Type | Tipo de documento |
| 7 | `DocumentSubType` | Edm.String | Yes | Document Sub Type | Subtipo de documento |
