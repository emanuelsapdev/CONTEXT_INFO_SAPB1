# ServiceContract_Line — Líneas del contrato de servicio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ServiceContract_Line`
- **Descripción (ES):** Líneas del contrato de servicio
- **Description (EN):** Service Contract Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `ManufacturerSerialNum` | Edm.String | Yes | Manufacturer Serial Number | Número de serie del fabricante |
| 3 | `InternalSerialNum` | Edm.String | Yes | Internal Serial Number | Número de serie interno |
| 4 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 5 | `ItemName` | Edm.String | Yes | Item Name | Nombre del artículo |
| 6 | `ItemGroup` | Edm.Int32 | Yes | Item Group | Grupo de artículos |
| 7 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 8 | `EndDate` | Edm.DateTimeOffset | Yes | End Date | Fecha de fin |
| 9 | `ItemGroupName` | Edm.String | Yes | Item Group Name | Nombre del grupo de artículos |
| 10 | `TerminationDate` | Edm.DateTimeOffset | Yes | Termination Date | Fecha de terminación |

## Used by (properties)

- [ServiceContract](../Entidades/ServiceContracts.md).`ServiceContract_Lines`
