# BoGSTRegnTypeEnum — Tipo de registro GST (India)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoGSTRegnTypeEnum`
- **Descripción (ES):** Tipo de registro GST (India)
- **Underlying type:** Edm.Int32
- **Members:** 7

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `invalid` | 0 | Invalid | Inválido |
| `gstRegularTDSISD` | 1 | Regular TDSISD | Regular/TDS/ISD |
| `gstCasualTaxablePerson` | 2 | Casual Taxable Person | Contribuyente ocasional |
| `gstCompositionLevy` | 3 | Composition Levy | Régimen de composición |
| `gstGoverDepartPSU` | 4 | Gover Depart PSU | Departamento gubernamental/PSU |
| `gstNonResidentTaxablePerson` | 5 | Non Resident Taxable Person | Contribuyente no residente |
| `gstUNAgencyEmbassy` | 6 | UN Agency Embassy | Agencia de la ONU/embajada |

## Used by (2 properties)

- [BPAddress](../Tipos-Complejos/BPAddress.md).`GstType`
- [WarehouseLocation](../Entidades/WarehouseLocations.md).`GstType`
