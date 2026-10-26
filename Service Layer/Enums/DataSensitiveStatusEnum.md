# DataSensitiveStatusEnum — Estado de datos sensibles

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `DataSensitiveStatusEnum`
- **Descripción (ES):** Estado de datos sensibles
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `dss_FieldNotSentive` | 0 | Field Not Sentive | Campo no sensible |
| `dss_DataSubjectNotNaturalPerson` | 1 | Data Subject Not Natural Person | El titular no es persona física |
| `dss_DataSubjectIsBlockedOrErased` | 2 | Data Subject Is Blocked Or Erased | El titular está bloqueado o borrado |
| `dss_DataIsSensitive` | 3 | Data Is Sensitive | Los datos son sensibles |
| `dss_Error` | 4 | Error | Error |
| `dss_TransactionIsErased` | 5 | Transaction Is Erased | La transacción está borrada |

## Used by (1 properties)

- [DataSensitiveStatus](../Tipos-Complejos/DataSensitiveStatus.md).`DataSensitiveStatusProperty`
