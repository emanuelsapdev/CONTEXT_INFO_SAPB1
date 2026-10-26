# BoAddressType — Tipo de dirección

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoAddressType`
- **Descripción (ES):** Tipo de dirección
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bo_ShipTo` | 0 | Ship To | Dirección de envío (S) |
| `bo_BillTo` | 1 | Bill To | Dirección de facturación (B) |

## Used by (6 properties)

- [Activity](../Entidades/Activities.md).`AddressType`
- [BPAddress](../Tipos-Complejos/BPAddress.md).`AddressType`
- [BPFiscalTaxID](../Tipos-Complejos/BPFiscalTaxID.md).`AddrType`
- [ContactEmployee](../Tipos-Complejos/ContactEmployee.md).`ConnectedAddressType`
- [ServiceCall](../Entidades/ServiceCalls.md).`AddressType`
- [ServiceCallScheduling](../Tipos-Complejos/ServiceCallScheduling.md).`AddressTypeBS`
