# SALOG - add-ons change log table

- **Tabla:** SALOG
- **Descripción:** add-ons change log table
- **Cantidad de campos:** 37
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SALOG.html

## Campos (37)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | Log ID | Int | 11 | - | -1 |  |
| 2 | `Operation` | DB Operation | nVarChar | 20 | - |  |  |
| 3 | `AddOnId` | AddOn ID | Int | 11 | - |  |  |
| 4 | `NameSpace` | Partner Name Space | nVarChar | 20 | - |  |  |
| 5 | `PName` | Partner Name | nVarChar | 40 | - |  |  |
| 6 | `AName` | AddOn Name | nVarChar | 40 | - |  |  |
| 7 | `EName` | AddOn Exe name | nVarChar | 128 | - |  |  |
| 8 | `CData` | Partner Contact Data | nVarChar | 80 | - |  |  |
| 9 | `AddOnChk` | AddOn Exe Check Sum | nVarChar | 32 | - |  |  |
| 10 | `InstName` | AddOn Installer Name | nVarChar | 128 | - |  |  |
| 11 | `InstChkSum` | AddOn Installer Check Sum | nVarChar | 32 | - |  |  |
| 12 | `InstTime` | Installation estimation time | Int | 11 | - |  |  |
| 13 | `AddOnVer` | AddOn Version | nVarChar | 20 | - |  |  |
| 14 | `ForceFlag` | AddOn Install force flag | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 15 | `UnInstName` | AddOn Uninstaller Name | nVarChar | 128 | - |  |  |
| 16 | `UnInstChk` | AddOn UnInstaller Check Sum | nVarChar | 32 | - |  |  |
| 17 | `UnInstPar` | UnInstaller params | nVarChar | 200 | - |  |  |
| 18 | `InstIsUn` | Is Installer is UnInstaller | VarChar | 1 | - |  |  |
| 19 | `AGroup` | AddOn Group | VarChar | 1 | - |  |  |
| 20 | `IParams` | Installer Params | nVarChar | 200 | - |  |  |
| 21 | `UnInstTime` | Uninstallation estimation time | Int | 11 | - | 0 |  |
| 22 | `AutoAssign` | Automatic Company Assignment | VarChar | 1 | - | N |  |
| 23 | `Visible` | AddOn is visible in AddOnAdmin | VarChar | 1 | - | Y | `Y` = Yes, visible<br>`N` |
| 24 | `SelfUpgrd` | Don`t install/uninstal | VarChar | 1 | - | N | `Y` = Yes, don`t install/uninstall<br>`N` = No, perform install/uninstall |
| 25 | `InstSil` | Use silent mode in install | VarChar | 1 | - | N | `Y` = Silent mode supported<br>`N` = Silent mode not supported |
| 26 | `UnInstSil` | Use silent mode in uninstall | VarChar | 1 | - | N | `Y` = Silent mode supported<br>`N` = Silent mode not supported |
| 27 | `UpgSil` | Use silent mode in upgrade | VarChar | 1 | - | N | `Y` = Silent mode supported<br>`N` = Silent mode not supported |
| 28 | `InstPFChk` | Checksum of install param file | nVarChar | 32 | - |  |  |
| 29 | `UnInstPFCh` | Checksum of uninstall par file | nVarChar | 32 | - |  |  |
| 30 | `UpgPFChk` | Checksum of upgrade param file | nVarChar | 32 | - |  |  |
| 31 | `UpgName` | Addon upgrader name | nVarChar | 128 | - |  |  |
| 32 | `UpgTime` | Estimated upgrade time | Int | 11 | - | 0 |  |
| 33 | `UpgParams` | Upgrader params | nVarChar | 200 | - |  |  |
| 34 | `UpgChkSum` | Addon upgrader checksum | nVarChar | 32 | - |  |  |
| 35 | `IsAdd64` | Is Addon Installer 64bit | VarChar | 1 | - | N |  |
| 36 | `AddPlat` | Platform of addon installer | VarChar | 1 | - | N | `N` = x86<br>`X` = x64 |
| 37 | `ClientType` | Client type supported by the addon | VarChar | 1 | - | W | `W` = Windows desktop<br>`B` = Browser access<br>`A` = All |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
