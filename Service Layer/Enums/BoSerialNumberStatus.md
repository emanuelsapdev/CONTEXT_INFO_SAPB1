# BoSerialNumberStatus — Estado del número de serie (tarjeta de equipo)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoSerialNumberStatus`
- **Descripción (ES):** Estado del número de serie (tarjeta de equipo)
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `sns_Active` | 0 | Active | Activo |
| `sns_Returned` | 1 | Returned | Devuelto |
| `sns_Terminated` | 2 | Terminated | Terminado |
| `sns_Loaned` | 3 | Loaned | Prestado |
| `sns_InLab` | 4 | In Lab | En laboratorio |

## Used by (1 properties)

- [CustomerEquipmentCard](../Entidades/CustomerEquipmentCards.md).`StatusOfSerialNumber`
