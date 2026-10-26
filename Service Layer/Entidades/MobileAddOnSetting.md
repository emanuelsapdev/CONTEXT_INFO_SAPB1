# MobileAddOnSetting — Configuración de add-on móvil

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `MobileAddOnSetting`
- **Descripción (ES):** Configuración de add-on móvil
- **Entity type:** `MobileAddOnSetting`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 11 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/MobileAddOnSetting?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/MobileAddOnSetting/$count` | Contar |
| Get by key | `GET /b1s/v2/MobileAddOnSetting('value')` | Obtener por clave |
| Create | `POST /b1s/v2/MobileAddOnSetting` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/MobileAddOnSetting('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/MobileAddOnSetting('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/MobileAddOnSetting('value')` (only if the B1 object allows removal) | Borrar |

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `Url` | Edm.String | Yes | Url | URL |
| 4 | `Type` | [MobileAddonSettingTypeEnum](../Enums/MobileAddonSettingTypeEnum.md) | Yes | Type | Tipo |
| 5 | `Provider` | Edm.String | Yes | Provider | Proveedor (de servicio) |
| 6 | `ViewStyle` | [ViewStyleTypeEnum](../Enums/ViewStyleTypeEnum.md) | Yes | View Style | Estilo de vista |
| 7 | `LogonMethod` | [LogonMethodEnum](../Enums/LogonMethodEnum.md) | Yes | Logon Method | Método de inicio de sesión |
| 8 | `Enable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable | Habilitar |
| 9 | `B1MobileApp` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | B 1 Mobile App | App móvil de SAP Business One |
| 10 | `B1SalesApp` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | B 1 Sales App | App de ventas de SAP Business One |
| 11 | `B1ServiceApp` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | B 1 Service App | App de servicio de SAP Business One |
