# SupportUserLoginRecordLogReasonTypeEnum — Motivo de inicio de sesión del usuario de soporte

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `SupportUserLoginRecordLogReasonTypeEnum`
- **Descripción (ES):** Motivo de inicio de sesión del usuario de soporte
- **Underlying type:** Edm.Int32
- **Members:** 11

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `reasonTransIssueAnaly` | 0 | Trans Issue Analy | Análisis de problema de transacción |
| `reasonSetupIssueAnaly` | 1 | Setup Issue Analy | Análisis de problema de configuración |
| `reasonDataIssueAnaly` | 2 | Data Issue Analy | Análisis de problema de datos |
| `reasonAddonIssueAnaly` | 3 | Addon Issue Analy | Análisis de problema de add-on |
| `reasonCustomerIssueAnaly` | 4 | Customer Issue Analy | Análisis de problema del cliente |
| `reasonSystemMaint` | 5 | System Maint | Mantenimiento del sistema |
| `reasonConsulting` | 6 | Consulting | Consultoría |
| `reasonOther` | 7 | Other | Otro |
| `reasonAddonAccess` | 8 | Addon Access | Acceso de add-on |
| `reasonRootCauseAnaly` | 9 | Root Cause Analy | Análisis de causa raíz |
| `reasonConsultSupport` | 10 | Consult Support | Soporte de consultoría |

## Used by (1 properties)

- [SupportUserLoginRecord](../Tipos-Complejos/SupportUserLoginRecord.md).`LogReason`
