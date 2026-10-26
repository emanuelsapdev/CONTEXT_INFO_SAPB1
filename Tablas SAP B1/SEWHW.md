# SEWHW - SEWHW

- **Tabla:** SEWHW
- **Descripción:** SEWHW
- **Cantidad de campos:** 23
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SEWHW.html

## Campos (23)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MachineNam` | Machine Name | nVarChar | 254 | - |  |  |
| 2 | `CompDbNam` | Company Db Name | nVarChar | 200 | - |  |  |
| 3 | `SmpTableId` | Smp Table ID | nVarChar | 3 | - |  |  |
| 4 | `EwaSentDat` | EWA Sent Date | nVarChar | 10 | - |  |  |
| 5 | `CustNumber` | Customer Number | nVarChar | 100 | - |  |  |
| 6 | `OsType` | OS Type | nVarChar | 64 | - |  |  |
| 7 | `OsVersion` | OS Version | nVarChar | 32 | - |  |  |
| 8 | `VendorIden` | Vendor Identity | nVarChar | 254 | - |  |  |
| 9 | `CpuType` | CPU TYPE | nVarChar | 32 | - |  |  |
| 10 | `NumOfCPUs` | Number Of CPUs | Int | 11 | - |  |  |
| 11 | `PhysMemory` | Physical Memory | Int | 11 | - |  |  |
| 12 | `ServerFlag` | Server Flag (Is Server?) | VarChar | 1 | - |  | `0` = No<br>`1` = Yes |
| 13 | `TotDskSpac` | Total Disk Space | nVarChar | 16 | - |  |  |
| 14 | `FreDskSpac` | Free Disk Space | nVarChar | 16 | - |  |  |
| 15 | `UseDskSpac` | Used Disk Space | nVarChar | 16 | - |  |  |
| 16 | `CRRntmVer` | CR Runtime Version | nVarChar | 100 | - |  |  |
| 17 | `BOBIPltVer` | BO BI Platform Version | nVarChar | 100 | - |  |  |
| 18 | `CRDsgnrVer` | CR Designer Version | nVarChar | 100 | - |  |  |
| 19 | `CRIntPgVer` | CR Integration Package Version | nVarChar | 100 | - |  |  |
| 20 | `NETFrmVer` | .NET Framework Version | nVarChar | 254 | - |  |  |
| 21 | `NETFrmSDKV` | .NET Framework SDK Version | nVarChar | 254 | - |  |  |
| 22 | `MmrMngSett` | Memory Management Settings | nVarChar | 254 | - |  |  |
| 23 | `B1ClntPltf` | BusinessOne Client Platform | nVarChar | 10 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MachineNam, CompDbNam |
