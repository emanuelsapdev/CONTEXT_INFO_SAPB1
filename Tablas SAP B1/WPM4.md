# WPM4 - Process Map Action

- **Tabla:** WPM4
- **Descripción:** Process Map Action
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WPM4.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PrcMapId` | Process Map ID | nVarChar | 40 | [OWPM](OWPM.md) |  |  |
| 2 | `StepId` | Step ID | nVarChar | 40 | - |  |  |
| 3 | `Guid` | Guid of Action | nVarChar | 40 | - |  |  |
| 4 | `ObjName` | Object Name | nVarChar | 50 | - |  |  |
| 5 | `Name` | Action Name | nVarChar | 254 | - |  |  |
| 6 | `Button` | Button | nVarChar | 254 | - |  |  |
| 7 | `Type` | Action Type | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PrcMapId, StepId, Guid |
