# SEWIC - SEWIC

- **Tabla:** SEWIC
- **Descripción:** SEWIC
- **Cantidad de campos:** 41
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SEWIC.html

## Campos (41)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CompanyNam` | CompanyName | nVarChar | 200 | - |  |  |
| 2 | `SmpTableId` | Smp Table ID | nVarChar | 3 | - |  |  |
| 3 | `EwaSentDat` | EWA Sent Date | nVarChar | 10 | - |  |  |
| 4 | `EwaSentTim` | EWA Sent Time | nVarChar | 8 | - |  |  |
| 5 | `CustNumber` | Customer Number | VarChar | 1 | - |  |  |
| 6 | `CustName` | Customer Name | VarChar | 1 | - |  |  |
| 7 | `CustConPer` | Customer contact person | VarChar | 1 | - |  |  |
| 8 | `CustEmail` | Customer Email | nVarChar | 100 | - |  |  |
| 9 | `PartnerNam` | Partner Name | nVarChar | 200 | - |  |  |
| 10 | `PartConPer` | Partnercontact person | VarChar | 1 | - |  |  |
| 11 | `PartEmail` | Partner Email | nVarChar | 100 | - |  |  |
| 12 | `PartEmail2` | Partner Email 2 | VarChar | 1 | - |  |  |
| 13 | `CompDbName` | Company DB Name | nVarChar | 200 | - |  |  |
| 14 | `CompDbVer` | Compnay DB Version | nVarChar | 32 | - |  |  |
| 15 | `SentUser` | Sent User | nVarChar | 30 | - |  |  |
| 16 | `B1Version` | B1 Version | nVarChar | 32 | - |  |  |
| 17 | `B1Suppack` | B1 Support Pack | nVarChar | 128 | - |  |  |
| 18 | `B1Patch` | B1 Patch | nVarChar | 128 | - |  |  |
| 19 | `UiApiVer` | UI API Version | nVarChar | 32 | - |  |  |
| 20 | `InstallNum` | Installation Number | nVarChar | 128 | - |  |  |
| 21 | `SystemNum` | System Number | nVarChar | 128 | - |  |  |
| 22 | `LicenseNum` | License Number | nVarChar | 128 | - |  |  |
| 23 | `SystemStat` | System Status | VarChar | 1 | - |  |  |
| 24 | `DbType` | DB Type | nVarChar | 64 | - |  |  |
| 25 | `DbVersion` | DB Version | nVarChar | 32 | - |  |  |
| 26 | `CommLogPat` | SBo-Common Log Path | nVarChar | 254 | - |  |  |
| 27 | `CommLogSiz` | SBO-Common Log Size | Int | 11 | - |  |  |
| 28 | `CommRecovM` | SBO-Common Recovery Model | nVarChar | 32 | - |  |  |
| 29 | `AOFramewor` | Addon Framwork | VarChar | 1 | - |  |  |
| 30 | `AODtw` | Addon DTW | VarChar | 1 | - |  |  |
| 31 | `AOSupTools` | Addon Support Tools | nVarChar | 12 | - |  |  |
| 32 | `AODateV` | Addon Date V | nVarChar | 12 | - |  |  |
| 33 | `AOAld` | Addon Ald | nVarChar | 12 | - |  |  |
| 34 | `AOBcSets` | Addon BC Sets | nVarChar | 12 | - |  |  |
| 35 | `AOElster` | Addon Elster | nVarChar | 12 | - |  |  |
| 36 | `AOFixAsset` | Addon Fixed Assets | nVarChar | 12 | - |  |  |
| 37 | `AOIntrStat` | Addon Intra Stat | nVarChar | 12 | - |  |  |
| 38 | `AOOutlookI` | Addon Outlook integration | nVarChar | 12 | - |  |  |
| 39 | `AOPayEngin` | Addon Payment Engine | nVarChar | 12 | - |  |  |
| 40 | `AOStampIt` | Addon Stamp it | nVarChar | 12 | - |  |  |
| 41 | `CompRecovM` | Company Recover Model | nVarChar | 32 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CompDbName |
