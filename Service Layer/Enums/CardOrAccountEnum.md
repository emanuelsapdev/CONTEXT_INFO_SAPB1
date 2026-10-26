# CardOrAccountEnum — Socio de negocios o cuenta

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `CardOrAccountEnum`
- **Descripción (ES):** Socio de negocios o cuenta
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `coaCard` | 0 | Card | Socio de negocios |
| `coaAccount` | 1 | Account | Cuenta |

## Used by (3 properties)

- [InternalReconciliation](../Entidades/InternalReconciliations.md).`CardOrAccount`
- [InternalReconciliationOpenTrans](../Tipos-Complejos/InternalReconciliationOpenTrans.md).`CardOrAccount`
- [InternalReconciliationOpenTransParams](../Tipos-Complejos/InternalReconciliationOpenTransParams.md).`CardOrAccount`
