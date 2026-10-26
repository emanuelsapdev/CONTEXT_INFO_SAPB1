# SINF - Server Info

- **Tabla:** SINF
- **Descripción:** Server Info
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SINF.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Version` | Version | Int | 11 | - |  |  |
| 2 | `Flags` | Flags | nVarChar | 100 | - |  |  |
| 3 | `UpgCab` | Upg CAB | Text | 16 | - |  |  |
| 4 | `AppDate` | Application Date | Date | 8 | - |  |  |
| 5 | `ClusterID` | Cluster Identification | nVarChar | 3 | - |  |  |
| 6 | `AppTime` | Application Time | Int | 6 | - |  |  |
| 7 | `ShrPath` | Shared folder path | Text | 16 | - |  |  |
| 8 | `Algo` | Encryption Algorithm. | Int | 6 | - |  |  |
| 9 | `PatchLevel` | Application Patch Level | nVarChar | 50 | - |  |  |
| 10 | `BuildDesc` | Build Descriptor | nVarChar | 50 | - |  |  |
| 11 | `IsPALInit` | Is PAL Initialize or Not | VarChar | 1 | - | N |  |
| 12 | `FP` | Application Feature Pack | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Version |
