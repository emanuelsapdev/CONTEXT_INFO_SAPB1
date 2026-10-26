# EPSRV - EPSRV

- **Tabla:** EPSRV
- **Descripción:** EPSRV
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EPSRV.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | auto generated id | Identity | 11 | - |  |  |
| 2 | `PkgName` | FK to EPPKG table | nVarChar | 50 | - |  |  |
| 3 | `SrvName` | thee name of the service | nVarChar | 60 | - |  |  |
| 4 | `Namespace` | namespace of service in code | nVarChar | 100 | - |  |  |
| 5 | `SrvAddress` | the prefix url of the service | nVarChar | 254 | - |  |  |
| 6 | `InOut` | Service direction | nVarChar | 10 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
| IX_SERVICE | Yes | SrvName, Namespace |
| IX_ADDRESS | Yes | SrvAddress |
