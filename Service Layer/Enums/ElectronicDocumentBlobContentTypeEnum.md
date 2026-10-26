# ElectronicDocumentBlobContentTypeEnum — Tipo de contenido del documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ElectronicDocumentBlobContentTypeEnum`
- **Descripción (ES):** Tipo de contenido del documento electrónico
- **Underlying type:** Edm.Int32
- **Members:** 9

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `edbctDefault` | -1 | Default | Predeterminado |
| `edbctXML` | 0 | XML | XML |
| `edbctZippedXML` | 1 | Zipped XML | XML comprimido |
| `edbctJSON` | 2 | JSON | JSON |
| `edbctZippedJSON` | 3 | Zipped JSON | JSON comprimido |
| `edbctText` | 4 | Text | Texto |
| `edbctZippedP7M` | 5 | Zipped P 7 M | P7M comprimido |
| `edbctP7M` | 6 | P 7 M | P7M |
| `edbctZippedPDF` | 7 | Zipped PDF | PDF comprimido |

## Used by (2 properties)

- [EDFEntryAddLogInputParams](../Tipos-Complejos/EDFEntryAddLogInputParams.md).`LogDataContentType`
- [EDFEntryLogInputParams](../Tipos-Complejos/EDFEntryLogInputParams.md).`LogDataContentType`
