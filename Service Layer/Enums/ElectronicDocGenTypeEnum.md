# ElectronicDocGenTypeEnum — Tipo de generación de documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ElectronicDocGenTypeEnum`
- **Descripción (ES):** Tipo de generación de documento electrónico
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `edgt_NotRelevant` | 0 | Not Relevant | No relevante |
| `edgt_Generate` | 1 | Generate | Generar |
| `edgt_GenerateLater` | 2 | Generate Later | Generar más tarde |

## Used by (3 properties)

- [EDFEntry](../Tipos-Complejos/EDFEntry.md).`GenerationType`
- [ElectronicProtocol](../Tipos-Complejos/ElectronicProtocol.md).`GenerationType`
- [TransportationDocumentData](../Entidades/TransportationDocument.md).`ElDocGenType`
