# DocumentRemarksIncludeTypeEnum — Contenido de comentarios del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `DocumentRemarksIncludeTypeEnum`
- **Descripción (ES):** Contenido de comentarios del documento
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `driBaseDocumentNumber` | 0 | Base Document Number | Número del documento base |
| `driBPReferenceNumber` | 1 | Business Partner Reference Number | Número de referencia del socio de negocios |
| `driManualRemarksOnly` | 2 | Manual Remarks Only | Solo comentarios manuales |

## Used by (1 properties)

- [ExtendedAdminInfo](../Tipos-Complejos/ExtendedAdminInfo.md).`DocumentRemarksInclude`
