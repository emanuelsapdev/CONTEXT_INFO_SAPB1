# WPM2 - Process Map Relation

- **Tabla:** WPM2
- **Descripción:** Process Map Relation
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WPM2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PrcMapId` | Process Map ID | nVarChar | 40 | [OWPM](OWPM.md) |  |  |
| 2 | `Guid` | Guid of Relation | nVarChar | 40 | - |  |  |
| 3 | `FromId` | From ID | nVarChar | 40 | - |  |  |
| 4 | `ToId` | To ID | nVarChar | 40 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PrcMapId, Guid |
