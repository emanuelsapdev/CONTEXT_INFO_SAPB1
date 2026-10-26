# DataPrivacyProtectionEnum — Estado de protección de datos personales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `DataPrivacyProtectionEnum`
- **Descripción (ES):** Estado de protección de datos personales
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `dpp_None` | 0 | None | Ninguno |
| `dpp_Erased` | 1 | Erased | Borrado |
| `dpp_Blocked` | 2 | Blocked | Bloqueado |
| `dpp_Unblocked` | 3 | Unblocked | Desbloqueado |
