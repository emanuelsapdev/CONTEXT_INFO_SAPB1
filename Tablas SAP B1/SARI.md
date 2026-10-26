# SARI - SARI

- **Tabla:** SARI
- **Descripción:** SARI
- **Cantidad de campos:** 48
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SARI.html

## Campos (48)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AddOnId` | AddOn ID | Int | 11 | - | -1 |  |
| 2 | `NameSpace` | Partner Name Space | nVarChar | 20 | - |  |  |
| 3 | `PName` | Partner Name | nVarChar | 40 | - |  |  |
| 4 | `AName` | AddOn Name | nVarChar | 40 | - |  |  |
| 5 | `EName` | AddOn Exe name | nVarChar | 128 | - |  |  |
| 6 | `CData` | Partner Contact Data | nVarChar | 80 | - |  |  |
| 7 | `AddOnChk` | AddOn Exe Check Sum | nVarChar | 32 | - |  |  |
| 8 | `InstName` | AddOn Installer Name | nVarChar | 128 | - |  |  |
| 9 | `InstChkSum` | AddOn Installer Check Sum | nVarChar | 32 | - |  |  |
| 10 | `ABinary` | AddOn Installer Binary | Text | 16 | - |  |  |
| 11 | `InstTime` | Installation estimation time | Int | 11 | - |  |  |
| 12 | `AddOnVer` | AddOn Version | nVarChar | 20 | - |  |  |
| 13 | `ForceFlag` | AddOn Install force flag | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 14 | `UnInstName` | AddOn Uninstaller Name | nVarChar | 128 | - |  |  |
| 15 | `UnInstChk` | AddOn UnInstaller Check Sum | nVarChar | 32 | - |  |  |
| 16 | `UnInstPar` | UnInstaller params | nVarChar | 200 | - |  |  |
| 17 | `InstIsUn` | Is Installer is UnInstaller | VarChar | 1 | - |  |  |
| 18 | `AGroup` | AddOn Group | VarChar | 1 | - |  |  |
| 19 | `IParams` | Installer Params | nVarChar | 200 | - |  |  |
| 20 | `UnInstTime` | Uninstallation estimation time | Int | 11 | - | 0 |  |
| 21 | `AutoAssign` | Automatic Company Assignment | VarChar | 1 | - | N |  |
| 22 | `Visible` | AddOn is visible in AddOnAdmin | VarChar | 1 | - | Y | `Y` = Yes, visible<br>`N` |
| 23 | `SelfUpgrd` | Don`t install/uninstal | VarChar | 1 | - | N | `Y` = Yes, don`t install/uninstall<br>`N` = No, perform install/uninstall |
| 24 | `InstSil` | Use silent mode in install | VarChar | 1 | - | N | `Y` = Silent mode supported<br>`N` = Silent mode not supported |
| 25 | `UnInstSil` | Use silent mode in uninstall | VarChar | 1 | - | N | `Y` = Silent mode supported<br>`N` = Silent mode not supported |
| 26 | `UpgSil` | Use silent mode in upgrade | VarChar | 1 | - | N | `Y` = Silent mode supported<br>`N` = Silent mode not supported |
| 27 | `InstParF` | Parameter files in install | Text | 16 | - |  |  |
| 28 | `UnInstParF` | Parameter files in uninstall | Text | 16 | - |  |  |
| 29 | `UpgParF` | Parameter files in upgrade | Text | 16 | - |  |  |
| 30 | `InstPFChk` | Checksum of install param file | nVarChar | 32 | - |  |  |
| 31 | `UnInstPFCh` | Checksum of uninstall par file | nVarChar | 32 | - |  |  |
| 32 | `UpgPFChk` | Checksum of upgrade param file | nVarChar | 32 | - |  |  |
| 33 | `UpgName` | Addon upgrader name | nVarChar | 128 | - |  |  |
| 34 | `UpgTime` | Estimated upgrade time | Int | 11 | - | 0 |  |
| 35 | `UpgParams` | Upgrader params | nVarChar | 200 | - |  |  |
| 36 | `AUpgrader` | Addon upgrader binary | Text | 16 | - |  |  |
| 37 | `UpgChkSum` | Addon upgrader checksum | nVarChar | 32 | - |  |  |
| 38 | `ABinary64` | AddOn Installer Binary (64bit) | Text | 16 | - |  |  |
| 39 | `IsAdd64` | Is Addon Installer 64bit | VarChar | 1 | - | N |  |
| 40 | `AddPlat` | Platform of addon installer | VarChar | 1 | - | N | `N` = x86<br>`X` = x64 |
| 41 | `ClientType` | Client type supported by the addon | VarChar | 1 | - | W | `W` = Windows desktop<br>`B` = Browser access<br>`A` = All |
| 42 | `AddOnChkX` | AddOn Exe Check Sum SHA256 | nVarChar | 64 | - |  |  |
| 43 | `InstChkX` | Installer Check Sum SHA256 | nVarChar | 64 | - |  |  |
| 44 | `UnInstChkX` | UnInstaller Check Sum SHA256 | nVarChar | 64 | - |  |  |
| 45 | `InstPFChkX` | SHA256 of install param file | nVarChar | 64 | - |  |  |
| 46 | `UnInstPFCX` | SHA256 of uninstall par file | nVarChar | 64 | - |  |  |
| 47 | `UpgPFChkX` | SHA256 of upgrade param file | nVarChar | 64 | - |  |  |
| 48 | `UpgChkSumX` | upgrader checksum SHA256 | nVarChar | 64 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | NameSpace, AName, AddOnId, AddPlat |
