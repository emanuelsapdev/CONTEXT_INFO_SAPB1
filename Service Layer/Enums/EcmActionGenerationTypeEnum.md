# EcmActionGenerationTypeEnum — Tipo de generación de acción de comunicación electrónica

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `EcmActionGenerationTypeEnum`
- **Descripción (ES):** Tipo de generación de acción de comunicación electrónica
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `lgtNotRelevant` | 1 | Not Relevant | No relevante |
| `lasGenerateLater` | 2 | Generate Later | Generar más tarde |
| `lasGenerate` | 3 | Generate | Generar |

## Used by (1 properties)

- [EcmAction](../Tipos-Complejos/EcmAction.md).`GenerationType`
