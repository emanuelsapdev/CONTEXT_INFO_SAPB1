# UserAccessLogReasonIDTypeEnum — Motivo del registro de acceso de usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `UserAccessLogReasonIDTypeEnum`
- **Descripción (ES):** Motivo del registro de acceso de usuario
- **Underlying type:** Edm.Int32
- **Members:** 12

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `reasonPlanInitialSystConf` | 0 | Plan Initial Syst Conf | Planificado: configuración inicial del sistema |
| `reasonPlanSystConfChang` | 1 | Plan Syst Conf Chang | Planificado: cambio de configuración |
| `reasonPlanSystMaint` | 2 | Plan Syst Maint | Planificado: mantenimiento del sistema |
| `reasonPlanKnowlTrans2EndUsr` | 3 | Plan Knowl Trans 2 End Usr | Planificado: transferencia de conocimiento al usuario |
| `reasonUnplanRootCauseAnaly` | 4 | Unplan Root Cause Analy | No planificado: análisis de causa raíz |
| `reasonUnplanKnowlTrans2EndUsr` | 5 | Unplan Knowl Trans 2 End Usr | No planificado: transferencia de conocimiento al usuario |
| `reasonUnplanSystMaint` | 6 | Unplan Syst Maint | No planificado: mantenimiento del sistema |
| `reasonUnplanSystConfChang` | 7 | Unplan Syst Conf Chang | No planificado: cambio de configuración |
| `reasonSystMaint` | 8 | Syst Maint | Mantenimiento del sistema |
| `reasonRootCauseAnaly` | 9 | Root Cause Analy | Análisis de causa raíz |
| `reasonConsultSupport` | 10 | Consult Support | Soporte de consultoría |
| `reasonOther` | 11 | Other | Otro |

## Used by (1 properties)

- [UserAccessLog](../Tipos-Complejos/UserAccessLog.md).`ReasonID`
