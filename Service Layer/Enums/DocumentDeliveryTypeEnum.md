# DocumentDeliveryTypeEnum — Tipo de entrega del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `DocumentDeliveryTypeEnum`
- **Descripción (ES):** Tipo de entrega del documento
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ddtNoneSeleted` | 0 | None Seleted | Ninguno seleccionado |
| `ddtCreateOnlineDocument` | 1 | Create Online Document | Crear documento en línea |
| `ddtPostToAribaNetwork` | 2 | Post To Ariba Network | Publicar en Ariba Network |

## Used by (1 properties)

- [Document](../Entidades/PurchaseQuotations.md).`DocumentDelivery`
