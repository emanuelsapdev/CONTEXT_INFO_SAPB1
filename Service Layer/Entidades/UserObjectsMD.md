# UserObjectsMD — Metadatos de objetos de usuario (UDO)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `UserObjectsMD`
- **Descripción (ES):** Metadatos de objetos de usuario (UDO)
- **Entity type:** `UserObjectsMD` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OUDO](../../Tablas%20SAP%20B1/OUDO.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 31 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/UserObjectsMD?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/UserObjectsMD/$count` | Contar |
| Get by key | `GET /b1s/v2/UserObjectsMD('value')` | Obtener por clave |
| Create | `POST /b1s/v2/UserObjectsMD` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/UserObjectsMD('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/UserObjectsMD('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/UserObjectsMD('value')` (only if the B1 object allows removal) | Borrar |

## Properties (31)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TableName` | Edm.String | Yes | Table Name | Nombre de la tabla |
| 2 | `Code` 🔑 | Edm.String | No | Code | Código |
| 3 | `LogTableName` | Edm.String | Yes | Log Table Name | Nombre de la tabla de registro |
| 4 | `CanCreateDefaultForm` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Can Create Default Form | Puede crear formulario predeterminado |
| 5 | `ObjectType` | [BoUDOObjType](../Enums/BoUDOObjType.md) | Yes | Object Type | Tipo de objeto |
| 6 | `ExtensionName` | Edm.String | Yes | Extension Name | Nombre de la extensión |
| 7 | `CanCancel` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Can Cancel | Puede cancelarse |
| 8 | `CanDelete` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Can Delete | Puede eliminarse |
| 9 | `CanLog` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Can Log | Puede registrar historial |
| 10 | `ManageSeries` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Manage Series | Gestionar series |
| 11 | `CanFind` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Can Find | Puede buscarse |
| 12 | `CanYearTransfer` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Can Year Transfer | Puede traspasarse a fin de año |
| 13 | `Name` | Edm.String | Yes | Name | Nombre |
| 14 | `CanClose` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Can Close | Puede cerrarse |
| 15 | `OverwriteDllfile` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Overwrite Dllfile | Sobrescribir archivo DLL |
| 16 | `UseUniqueFormType` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Unique Form Type | Usar tipo de formulario único |
| 17 | `CanArchive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Can Archive | Puede archivarse |
| 18 | `MenuItem` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Menu Item | Elemento de menú |
| 19 | `MenuCaption` | Edm.String | Yes | Menu Caption | Título del menú |
| 20 | `FatherMenuID` | Edm.Int32 | Yes | Father Menu ID | ID del menú padre |
| 21 | `Position` | Edm.Int32 | Yes | Position | Posición/cargo |
| 22 | `MenuUID` | Edm.String | Yes | Menu UID | UID del menú |
| 23 | `EnableEnhancedForm` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Enhanced Form | Habilitar formulario mejorado |
| 24 | `RebuildEnhancedForm` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Rebuild Enhanced Form | Reconstruir formulario mejorado |
| 25 | `FormSRF` | Edm.String | Yes | Form SRF | Archivo SRF del formulario |
| 26 | `ApplyAuthorization` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Apply Authorization | Aplicar autorización |
| 27 | `PersonalDataProtection` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Personal Data Protection | Protección de datos personales |
| 28 | `UserObjectMD_ChildTables` | Collection([UserObjectMD_ChildTable](../Tipos-Complejos/UserObjectMD_ChildTable.md)) | Yes | User Object Metadata Child Tables | Tablas hijas del UDO |
| 29 | `UserObjectMD_FindColumns` | Collection([UserObjectMD_FindColumn](../Tipos-Complejos/UserObjectMD_FindColumn.md)) | Yes | User Object Metadata Find Columns | Columnas de búsqueda del UDO |
| 30 | `UserObjectMD_FormColumns` | Collection([UserObjectMD_FormColumn](../Tipos-Complejos/UserObjectMD_FormColumn.md)) | Yes | User Object Metadata Form Columns | Columnas del formulario del UDO |
| 31 | `UserObjectMD_EnhancedFormColumns` | Collection([UserObjectMD_EnhancedFormColumn](../Tipos-Complejos/UserObjectMD_EnhancedFormColumn.md)) | Yes | User Object Metadata Enhanced Form Columns | Columnas del formulario mejorado del UDO |

## Navigation properties (1)

Use `GET /b1s/v2/UserObjectsMD('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `UserTablesMD` | [UserTablesMD](../Entidades/UserTablesMD.md) | [UserTablesMD](UserTablesMD.md) | TableName → TableName | Metadatos de tablas de usuario (UDT) |
