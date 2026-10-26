# Resources — Recursos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Resources`
- **Descripción (ES):** Recursos
- **Entity type:** `Resource` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [ORSC](../../Tablas%20SAP%20B1/ORSC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 109 · **Navigation properties:** 4 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Resources?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Resources/$count` | Contar |
| Get by key | `GET /b1s/v2/Resources('value')` | Obtener por clave |
| Create | `POST /b1s/v2/Resources` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Resources('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Resources('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/Resources('value')` (only if the B1 object allows removal) | Borrar |
| Action `CreateLinkedItem` | `POST /b1s/v2/Resources('value')/CreateLinkedItem` | Crear artículo vinculado |

## Properties (109)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `VisCode` | Edm.String | Yes | Vis Code | Código de visualización |
| 3 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 4 | `Number` | Edm.Int32 | Yes | Number | Número |
| 5 | `CodeBar` | Edm.String | Yes | Code Bar | Código de barras |
| 6 | `Name` | Edm.String | Yes | Name | Nombre |
| 7 | `ForeignName` | Edm.String | Yes | Foreign Name | Nombre extranjero |
| 8 | `Type` | [ResourceTypeEnum](../Enums/ResourceTypeEnum.md) | Yes | Type | Tipo |
| 9 | `Group` | Edm.Int32 | Yes | Group | Grupo |
| 10 | `UnitOfMeasure` | Edm.String | Yes | Unit Of Measure | Unidad de medida |
| 11 | `IssueMethod` | [ResourceIssueMethodEnum](../Enums/ResourceIssueMethodEnum.md) | Yes | Issue Method | Método de emisión (manual/notificación) |
| 12 | `Cost1` | Edm.Double | Yes | Cost 1 | Costo 1 |
| 13 | `Cost2` | Edm.Double | Yes | Cost 2 | Costo 2 |
| 14 | `Cost3` | Edm.Double | Yes | Cost 3 | Costo 3 |
| 15 | `Cost4` | Edm.Double | Yes | Cost 4 | Costo 4 |
| 16 | `Cost5` | Edm.Double | Yes | Cost 5 | Costo 5 |
| 17 | `Cost6` | Edm.Double | Yes | Cost 6 | Costo 6 |
| 18 | `Cost7` | Edm.Double | Yes | Cost 7 | Costo 7 |
| 19 | `Cost8` | Edm.Double | Yes | Cost 8 | Costo 8 |
| 20 | `Cost9` | Edm.Double | Yes | Cost 9 | Costo 9 |
| 21 | `Cost10` | Edm.Double | Yes | Cost 10 | Costo 10 |
| 22 | `Active` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active | Activo |
| 23 | `ActiveFrom` | Edm.DateTimeOffset | Yes | Active From | Activo desde |
| 24 | `ActiveTo` | Edm.DateTimeOffset | Yes | Active To | Activo hasta |
| 25 | `Inactive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inactive | Inactivo |
| 26 | `InactiveFrom` | Edm.DateTimeOffset | Yes | Inactive From | Inactivo desde |
| 27 | `InactiveTo` | Edm.DateTimeOffset | Yes | Inactive To | Inactivo hasta |
| 28 | `DefaultWarehouse` | Edm.String | Yes | Default Warehouse | Almacén predeterminado |
| 29 | `Picture` | Edm.String | Yes | Picture | Imagen |
| 30 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 31 | `Property1` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 1 | Propiedad 1 |
| 32 | `Property2` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 2 | Propiedad 2 |
| 33 | `Property3` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 3 | Propiedad 3 |
| 34 | `Property4` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 4 | Propiedad 4 |
| 35 | `Property5` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 5 | Propiedad 5 |
| 36 | `Property6` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 6 | Propiedad 6 |
| 37 | `Property7` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 7 | Propiedad 7 |
| 38 | `Property8` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 8 | Propiedad 8 |
| 39 | `Property9` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 9 | Propiedad 9 |
| 40 | `Property10` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 10 | Propiedad 10 |
| 41 | `Property11` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 11 | Propiedad 11 |
| 42 | `Property12` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 12 | Propiedad 12 |
| 43 | `Property13` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 13 | Propiedad 13 |
| 44 | `Property14` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 14 | Propiedad 14 |
| 45 | `Property15` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 15 | Propiedad 15 |
| 46 | `Property16` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 16 | Propiedad 16 |
| 47 | `Property17` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 17 | Propiedad 17 |
| 48 | `Property18` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 18 | Propiedad 18 |
| 49 | `Property19` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 19 | Propiedad 19 |
| 50 | `Property20` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 20 | Propiedad 20 |
| 51 | `Property21` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 21 | Propiedad 21 |
| 52 | `Property22` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 22 | Propiedad 22 |
| 53 | `Property23` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 23 | Propiedad 23 |
| 54 | `Property24` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 24 | Propiedad 24 |
| 55 | `Property25` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 25 | Propiedad 25 |
| 56 | `Property26` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 26 | Propiedad 26 |
| 57 | `Property27` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 27 | Propiedad 27 |
| 58 | `Property28` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 28 | Propiedad 28 |
| 59 | `Property29` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 29 | Propiedad 29 |
| 60 | `Property30` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 30 | Propiedad 30 |
| 61 | `Property31` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 31 | Propiedad 31 |
| 62 | `Property32` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 32 | Propiedad 32 |
| 63 | `Property33` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 33 | Propiedad 33 |
| 64 | `Property34` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 34 | Propiedad 34 |
| 65 | `Property35` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 35 | Propiedad 35 |
| 66 | `Property36` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 36 | Propiedad 36 |
| 67 | `Property37` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 37 | Propiedad 37 |
| 68 | `Property38` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 38 | Propiedad 38 |
| 69 | `Property39` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 39 | Propiedad 39 |
| 70 | `Property40` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 40 | Propiedad 40 |
| 71 | `Property41` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 41 | Propiedad 41 |
| 72 | `Property42` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 42 | Propiedad 42 |
| 73 | `Property43` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 43 | Propiedad 43 |
| 74 | `Property44` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 44 | Propiedad 44 |
| 75 | `Property45` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 45 | Propiedad 45 |
| 76 | `Property46` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 46 | Propiedad 46 |
| 77 | `Property47` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 47 | Propiedad 47 |
| 78 | `Property48` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 48 | Propiedad 48 |
| 79 | `Property49` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 49 | Propiedad 49 |
| 80 | `Property50` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 50 | Propiedad 50 |
| 81 | `Property51` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 51 | Propiedad 51 |
| 82 | `Property52` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 52 | Propiedad 52 |
| 83 | `Property53` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 53 | Propiedad 53 |
| 84 | `Property54` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 54 | Propiedad 54 |
| 85 | `Property55` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 55 | Propiedad 55 |
| 86 | `Property56` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 56 | Propiedad 56 |
| 87 | `Property57` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 57 | Propiedad 57 |
| 88 | `Property58` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 58 | Propiedad 58 |
| 89 | `Property59` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 59 | Propiedad 59 |
| 90 | `Property60` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 60 | Propiedad 60 |
| 91 | `Property61` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 61 | Propiedad 61 |
| 92 | `Property62` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 62 | Propiedad 62 |
| 93 | `Property63` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 63 | Propiedad 63 |
| 94 | `Property64` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Property 64 | Propiedad 64 |
| 95 | `ActiveRemarks` | Edm.String | Yes | Active Remarks | Observaciones de activo |
| 96 | `InactiveRemarks` | Edm.String | Yes | Inactive Remarks | Comentarios de inactividad |
| 97 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 98 | `UnitsPerTime` | Edm.Int32 | Yes | Units Per Time | Unidades por tiempo |
| 99 | `TimePerUnits` | Edm.Int32 | Yes | Time Per Units | Tiempo por unidades |
| 100 | `Allocation` | [ResourceAllocationEnum](../Enums/ResourceAllocationEnum.md) | Yes | Allocation | Asignación |
| 101 | `LinkedItem` | Edm.String | Yes | Linked Item | Artículo vinculado |
| 102 | `RelevantForSingleRun1` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Relevant For Single Run 1 | Relevante para ejecución única 1 |
| 103 | `RelevantForSingleRun2` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Relevant For Single Run 2 | Relevante para ejecución única 2 |
| 104 | `RelevantForSingleRun3` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Relevant For Single Run 3 | Relevante para ejecución única 3 |
| 105 | `RelevantForSingleRun4` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Relevant For Single Run 4 | Relevante para ejecución única 4 |
| 106 | `ResourceWarehouses` | Collection([ResourceWarehouse](../Tipos-Complejos/ResourceWarehouse.md)) | Yes | Resource Warehouses | Almacenes del recurso |
| 107 | `ResourceFixedAssets` | Collection([ResourceFixedAsset](../Tipos-Complejos/ResourceFixedAsset.md)) | Yes | Resource Fixed Assets | Activos fijos del recurso |
| 108 | `ResourceEmployees` | Collection([ResourceEmployee](../Tipos-Complejos/ResourceEmployee.md)) | Yes | Resource Employees | Empleados del recurso |
| 109 | `ResourceDailyCapacities` | Collection([ResourceDailyCapacity](../Tipos-Complejos/ResourceDailyCapacity.md)) | Yes | Resource Daily Capacities | Capacidades diarias del recurso |

## Navigation properties (4)

Use `GET /b1s/v2/Resources('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `ResourceCapacities` | Collection([ResourceCapacity](../Entidades/ResourceCapacities.md)) | [ResourceCapacities](ResourceCapacities.md) |  | Capacidades de recursos |
| `ResourceGroup` | [ResourceGroup](../Entidades/ResourceGroups.md) | [ResourceGroups](ResourceGroups.md) | Group → Code | Grupos de recursos |
| `Item` | [Item](../Entidades/Items.md) | [Items](Items.md) | LinkedItem → ItemCode | Artículos |

## Bound actions (1)

### CreateLinkedItem

- **Descripción (ES):** Crear artículo vinculado
- **Request:** `POST /b1s/v2/Resources('value')/CreateLinkedItem`

