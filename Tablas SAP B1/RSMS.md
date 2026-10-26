# RSMS - Resource Merged Snapshots List

- **Tabla:** RSMS
- **Descripción:** Resource Merged Snapshots List
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RSMS.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SourceDB` | Source DB | Int | 11 | - |  |  |
| 2 | `TargetDB` | Target DB | Int | 11 | - |  |  |
| 3 | `BaseServer` | Base Server Name | nVarChar | 254 | - |  |  |
| 4 | `BaseDB` | Base DB Name | nVarChar | 254 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SourceDB, TargetDB |
| BASE_DB | Yes | BaseServer, BaseDB |
