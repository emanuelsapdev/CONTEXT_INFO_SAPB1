# MDC2 - Master Data Cleanup - MD Log

- **Tabla:** MDC2
- **Descripción:** Master Data Cleanup - MD Log
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MDC2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [OMDC](OMDC.md) |  |  |
| 2 | `ObjectType` | Object Type | nVarChar | 20 | - |  |  |
| 3 | `UserAction` | User Action | VarChar | 1 | - |  | `O` = Original Recommendation<br>`D` = Deactivate |
| 4 | `DelContent` | Delete Content List | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, ObjectType |
