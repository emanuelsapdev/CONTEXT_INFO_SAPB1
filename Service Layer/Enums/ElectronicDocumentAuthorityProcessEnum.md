# ElectronicDocumentAuthorityProcessEnum — Proceso de la autoridad sobre el documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ElectronicDocumentAuthorityProcessEnum`
- **Descripción (ES):** Proceso de la autoridad sobre el documento electrónico
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `edapNone` | -1 | None | Ninguno |
| `edapApproval` | 0 | Approval | Aprobación |
| `edapRejection` | 1 | Rejection | Rechazo |

## Used by (3 properties)

- [EDFEntryAddLogInputParams](../Tipos-Complejos/EDFEntryAddLogInputParams.md).`AuthorityProcess`
- [EDFEntryLog](../Tipos-Complejos/EDFEntryLog.md).`AuthorityProcess`
- [EcmActionLog](../Tipos-Complejos/EcmActionLog.md).`AuthorityProcess`
