# SFMD - SFMD

- **Tabla:** SFMD
- **Descripción:** SFMD
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SFMD.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Version` | Version | Int | 11 | - |  |  |
| 2 | `Metadefs` | Metadefs.bin | Text | 16 | - |  |  |
| 3 | `ClusterID` | Cluster Identification | nVarChar | 3 | - |  |  |
| 4 | `PatchLevel` | Application Patch Level | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Version |
