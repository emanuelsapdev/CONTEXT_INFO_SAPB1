# BoUniqueSerialNumber — Número de serie único por

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoUniqueSerialNumber`
- **Descripción (ES):** Número de serie único por
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `usn_None` | 0 | None | Ninguno |
| `usn_MfrSerialNumber` | 1 | Mfr Serial Number | Número de serie del fabricante |
| `usn_SerialNumber` | 2 | Serial Number | Número de serie |
| `usn_LotNumber` | 3 | Lot Number | Número de lote |

## Used by (1 properties)

- [AdminInfo](../Tipos-Complejos/AdminInfo.md).`UniqueSerialNo`
