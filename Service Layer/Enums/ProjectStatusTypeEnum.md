# ProjectStatusTypeEnum — Estado del proyecto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ProjectStatusTypeEnum`
- **Descripción (ES):** Estado del proyecto
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `pst_Started` | 0 | Started | Iniciado |
| `pst_Paused` | 1 | Paused | En pausa |
| `pst_Stopped` | 2 | Stopped | Detenido |
| `pst_Finished` | 3 | Finished | Finalizado |
| `pst_Canceled` | 4 | Canceled | Cancelado |

## Used by (1 properties)

- [PM_ProjectDocumentData](../Entidades/ProjectManagements.md).`ProjectStatus`
