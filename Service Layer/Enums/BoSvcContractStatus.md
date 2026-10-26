# BoSvcContractStatus — Estado del contrato de servicio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoSvcContractStatus`
- **Descripción (ES):** Estado del contrato de servicio
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `scs_Approved` | 0 | Approved | Aprobado |
| `scs_Frozen` | 1 | Frozen | Congelado |
| `scs_Draft` | 2 | Draft | Borrador |
| `scs_Terminated` | 3 | Terminated | Terminado |

## Used by (1 properties)

- [ServiceContract](../Entidades/ServiceContracts.md).`Status`
