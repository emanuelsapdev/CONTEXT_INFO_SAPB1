# FormPreferences — Preferencias de formularios (columnas)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `FormPreferences`
- **Descripción (ES):** Preferencias de formularios (columnas)
- **Entity type:** `ColumnPreferences`
- **Key:** `User` (Edm.Int32), `FormID` (Edm.String), `ItemNumber` (Edm.String), `Column` (Edm.String)
- **DB tables (main / lines):** [CPRF](../../Tablas%20SAP%20B1/CPRF.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 11 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/FormPreferences?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/FormPreferences/$count` | Contar |
| Get by key | `GET /b1s/v2/FormPreferences(User=1,FormID='value',ItemNumber='value',Column='value')` | Obtener por clave |
| Create | `POST /b1s/v2/FormPreferences` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/FormPreferences(User=1,FormID='value',ItemNumber='value',Column='value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/FormPreferences(User=1,FormID='value',ItemNumber='value',Column='value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/FormPreferences(User=1,FormID='value',ItemNumber='value',Column='value')` (only if the B1 object allows removal) | Borrar |

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `User` 🔑 | Edm.Int32 | No | User | Usuario |
| 2 | `FormID` 🔑 | Edm.String | No | Form ID | ID de formulario |
| 3 | `ItemNumber` 🔑 | Edm.String | No | Item Number | Número de artículo |
| 4 | `Column` 🔑 | Edm.String | No | Column | Columna |
| 5 | `Width` | Edm.Int32 | Yes | Width | Ancho |
| 6 | `VisibleInForm` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Visible In Form | Visible en formulario |
| 7 | `TabsLayout` | Edm.Int32 | Yes | Tabs Layout | Diseño de pestañas |
| 8 | `EditableInForm` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Editable In Form | Editable en formulario |
| 9 | `VisibleInExpanded` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Visible In Expanded | Visible en vista expandida |
| 10 | `ExpandedIndex` | Edm.Int32 | Yes | Expanded Index | Índice expandido |
| 11 | `EditableInExpanded` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Editable In Expanded | Editable en vista expandida |

## Navigation properties (1)

Use `GET /b1s/v2/FormPreferences(User=1,FormID='value',ItemNumber='value',Column='value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `User2` | [User](../Entidades/Users.md) | [Users](Users.md) | User → InternalKey | Usuario 2 |
