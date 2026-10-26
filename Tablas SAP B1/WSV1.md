# WSV1 - Web Client Linked View Filter

- **Tabla:** WSV1
- **Descripción:** Web Client Linked View Filter
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WSV1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Guid` | GUID | nVarChar | 40 | - |  |  |
| 2 | `ParentId` | Parent Id | nVarChar | 40 | [OWSV](OWSV.md) |  |  |
| 3 | `FlterFld` | Filter Name | nVarChar | 254 | - |  |  |
| 4 | `BindField` | Bind Field | nVarChar | 254 | - |  |  |
| 5 | `CardId` | Card Id | nVarChar | 40 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ParentId, Guid |
