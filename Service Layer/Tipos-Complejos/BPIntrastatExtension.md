# BPIntrastatExtension — Extensión Intrastat del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BPIntrastatExtension`
- **Descripción (ES):** Extensión Intrastat del socio de negocios
- **Description (EN):** Business Partner Intrastat Extension

- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 2 | `TransportMode` | Edm.Int32 | Yes | Transport Mode | Modo de transporte |
| 3 | `Incoterms` | Edm.Int32 | Yes | Incoterms | Incoterms |
| 4 | `NatureOfTransactions` | Edm.Int32 | Yes | Nature Of Transactions | Naturaleza de las transacciones |
| 5 | `StatisticalProcedure` | Edm.Int32 | Yes | Statistical Procedure | Procedimiento estadístico |
| 6 | `CustomsProcedure` | Edm.Int32 | Yes | Customs Procedure | Procedimiento aduanero |
| 7 | `PortOfEntryOrExit` | Edm.Int32 | Yes | Port Of Entry Or Exit | Puerto de entrada o salida |
| 8 | `DomesticOrForeignID` | Edm.String | Yes | Domestic Or Foreign ID | ID nacional o extranjero |
| 9 | `IntrastatRelevant` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Intrastat Relevant | Relevante para Intrastat |

## Used by (properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`BPIntrastatExtension`
