# WPM1 - Process Map Step

- **Tabla:** WPM1
- **Descripción:** Process Map Step
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WPM1.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PrcMapId` | Process Map ID | nVarChar | 40 | [OWPM](OWPM.md) |  |  |
| 2 | `Guid` | Guid of Step | nVarChar | 40 | - |  |  |
| 3 | `Name` | Step Name | nVarChar | 254 | - |  |  |
| 4 | `Icon` | Icon | nVarChar | 254 | - |  |  |
| 5 | `ObjName` | Object Name | nVarChar | 50 | - |  |  |
| 6 | `Type` | Step Type | nVarChar | 50 | - |  |  |
| 7 | `ViewGuid` | View Guid | nVarChar | 40 | [OWVT](OWVT.md) |  |  |
| 8 | `ViewQuery` | View Query | Text | 16 | - |  |  |
| 9 | `ListUrl` | List Url | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PrcMapId, Guid |
