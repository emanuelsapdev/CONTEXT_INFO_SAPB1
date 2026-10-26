# LegalDataDetail — Detalle de datos legales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `LegalDataDetail`
- **Descripción (ES):** Detalle de datos legales
- **Description (EN):** Legal Data Detail

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineSequence` | Edm.Int32 | Yes | Line Sequence | Secuencia de línea |
| 3 | `LineType` | [LegalDataLineTypeEnum](../Enums/LegalDataLineTypeEnum.md) | Yes | Line Type | Tipo de línea |
| 4 | `TaxCode` | Edm.String | Yes | Tax Code | Indicador de impuesto |
| 5 | `TaxRate` | Edm.Double | Yes | Tax Rate | Tasa de impuesto |
| 6 | `Amount` | Edm.Double | Yes | Amount | Importe |

## Used by (properties)

- [LegalData](../Entidades/LegalData.md).`LegalDataDetailCollection`
