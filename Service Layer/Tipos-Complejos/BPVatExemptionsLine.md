# BPVatExemptionsLine — Líneas de exenciones de IVA del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BPVatExemptionsLine`
- **Descripción (ES):** Líneas de exenciones de IVA del socio de negocios
- **Description (EN):** Business Partner Vat Exemptions Line

- **Properties:** 15

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsoluteEntry` | Edm.Int32 | Yes | Absolute Entry | Entrada absoluta (ID interno) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `ExemptionDocNum` | Edm.String | Yes | Exemption Document Number | N.º de documento de exención |
| 4 | `IssueDate` | Edm.DateTimeOffset | Yes | Issue Date | Fecha de emisión |
| 5 | `IssueTime` | Edm.TimeOfDay | Yes | Issue Time | Hora de emisión |
| 6 | `ExemptionType` | Edm.Int32 | Yes | Exemption Type | Tipo de exención |
| 7 | `ApplyAllItems` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Apply All Items | Aplicar a todos los artículos |
| 8 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 9 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 10 | `VATRate` | Edm.Double | Yes | VAT Rate | Tasa de IVA |
| 11 | `TaxCode` | Edm.String | Yes | Tax Code | Indicador de impuesto |
| 12 | `AuthoritiesName` | Edm.String | Yes | Authorities Name | Nombre de la autoridad |
| 13 | `ValidFrom` | Edm.DateTimeOffset | Yes | Valid From | Válido desde |
| 14 | `ValidTo` | Edm.DateTimeOffset | Yes | Valid To | Válido hasta |
| 15 | `VisualOrder` | Edm.Int32 | Yes | Visual Order | Orden visual |

## Used by (properties)

- [BPVatExemptions](../Entidades/BPVatExemptions.md).`BPVatExemptionsLines`
