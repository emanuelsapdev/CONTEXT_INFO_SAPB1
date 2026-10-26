# OWVT - List View Variants

- **Tabla:** OWVT
- **Descripción:** List View Variants
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWVT.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Guid` | Guid | nVarChar | 40 | - |  |  |
| 2 | `Order` | Order | Int | 11 | - |  |  |
| 3 | `UserId` | User Id | Int | 11 | - |  |  |
| 4 | `ViewType` | View Type | nVarChar | 50 | - |  |  |
| 5 | `SubVType` | Sub View Type | nVarChar | 50 | - |  |  |
| 6 | `ViewId` | View Id | nVarChar | 50 | - | -1 |  |
| 7 | `ObjName` | Object Name | nVarChar | 50 | - |  |  |
| 8 | `FltBarLout` | FilterBarLayout | Text | 16 | - |  |  |
| 9 | `SysFilter` | System Filter | Text | 16 | - |  |  |
| 10 | `UserFilter` | User Filter | Text | 16 | - |  |  |
| 11 | `CdtFilter` | Condition Filter | Text | 16 | - |  |  |
| 12 | `IsPublic` | Is Public | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `IsSys` | Is System | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `Name` | Variant Name | nVarChar | 100 | - |  |  |
| 15 | `Version` | Version | Int | 11 | - |  |  |
| 16 | `OvpCus` | Overview Customization | Text | 16 | - |  |  |
| 17 | `ChartCus` | Chart Customization | Text | 16 | - |  |  |
| 18 | `ReportCus` | Report Customization | Text | 16 | - |  |  |
| 19 | `UserCus` | User Customization | Text | 16 | - |  |  |
| 20 | `UdqCus` | Udq Customization | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Guid |
| GROUP | No | UserId, ViewType, ViewId, ObjName |
