# StageDepTypeEnum — Tipo de dependencia de etapa

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `StageDepTypeEnum`
- **Descripción (ES):** Tipo de dependencia de etapa
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `sdt_Project` | 0 | Project | Proyecto |
| `sdt_Subproject` | 1 | Subproject | Subproyecto |

## Used by (8 properties)

- [PMS_StageData](../Tipos-Complejos/PMS_StageData.md).`StageDependency1Type`
- [PMS_StageData](../Tipos-Complejos/PMS_StageData.md).`StageDependency2Type`
- [PMS_StageData](../Tipos-Complejos/PMS_StageData.md).`StageDependency3Type`
- [PMS_StageData](../Tipos-Complejos/PMS_StageData.md).`StageDependency4Type`
- [PM_StageData](../Tipos-Complejos/PM_StageData.md).`StageDependency1Type`
- [PM_StageData](../Tipos-Complejos/PM_StageData.md).`StageDependency2Type`
- [PM_StageData](../Tipos-Complejos/PM_StageData.md).`StageDependency3Type`
- [PM_StageData](../Tipos-Complejos/PM_StageData.md).`StageDependency4Type`
