# WPM3 - Process Map External Action

- **Tabla:** WPM3
- **Descripción:** Process Map External Action
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WPM3.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PrcMapId` | Process Map ID | nVarChar | 40 | [OWPM](OWPM.md) |  |  |
| 2 | `StepId` | Step ID | nVarChar | 40 | - |  |  |
| 3 | `Guid` | Guid of External Action | nVarChar | 40 | - |  |  |
| 4 | `InputField` | Input Field | nVarChar | 50 | - |  |  |
| 5 | `Name` | External Action Name | nVarChar | 254 | - |  |  |
| 6 | `Infor` | Information | nVarChar | 254 | - |  |  |
| 7 | `Type` | External Action Type | nVarChar | 50 | - |  |  |
| 8 | `Link` | External URL Link | Text | 16 | - |  |  |
| 9 | `Remark` | Remark OR Notes | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PrcMapId, StepId, Guid |
