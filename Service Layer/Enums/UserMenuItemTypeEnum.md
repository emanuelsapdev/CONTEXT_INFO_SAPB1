# UserMenuItemTypeEnum — Tipo de elemento de menú de usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `UserMenuItemTypeEnum`
- **Descripción (ES):** Tipo de elemento de menú de usuario
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `umitForm` | 0 | Form | Formulario |
| `umitQuery` | 1 | Query | Consulta |
| `umitFolder` | 2 | Folder | Carpeta |
| `umitReport` | 3 | Report | Informe |
| `umitLink` | 4 | Link | Vínculo |

## Used by (1 properties)

- [UserMenuItem](../Tipos-Complejos/UserMenuItem.md).`Type`
