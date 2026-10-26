# ContractSequenceEnum — Periodicidad del contrato

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ContractSequenceEnum`
- **Descripción (ES):** Periodicidad del contrato
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `cs_Monthly` | 0 | Monthly | Mensual |
| `cs_Quarterly` | 1 | Quarterly | Trimestral |
| `cs_SemiAnnually` | 2 | Semi Annually | Semestral |
| `cs_Yearly` | 3 | Yearly | Anual |

## Used by (1 properties)

- [EmployeeSavingsPaymentInfo](../Tipos-Complejos/EmployeeSavingsPaymentInfo.md).`Sequence`
