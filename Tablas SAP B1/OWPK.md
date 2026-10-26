# OWPK - Dashboard Packages

- **Tabla:** OWPK
- **Descripción:** Dashboard Packages
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWPK.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `PackagCode` | Package Code | nVarChar | 32 | - |  |  |
| 3 | `PackagName` | Package Name | nVarChar | 100 | - |  |  |
| 4 | `Note` | Package Description | Text | 16 | - |  |  |
| 5 | `Content` | Package Content | Text | 16 | - |  |  |
| 6 | `Author` | Creator | nVarChar | 32 | - |  |  |
| 7 | `Version` | Version | nVarChar | 13 | - |  |  |
| 8 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 9 | `CreateTime` | Create Time | Int | 6 | - |  |  |
| 10 | `IsSystem` | Is System | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 11 | `PackagType` | Package Type | VarChar | 1 | - | D | `D` = Dashboard<br>`M` = Mobile<br>`P` = Pervasive |
| 12 | `ISIMDB` | IS IMDB | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 13 | `StraType` | Strategy Type | nVarChar | 254 | - | none |  |
| 14 | `StraPara` | Strategy Parameters | nVarChar | 254 | - |  |  |
| 15 | `SourceType` | Query Source Type | nVarChar | 20 | - | normal |  |
| 16 | `ViewName` | View's Name | nVarChar | 250 | - |  |  |
| 17 | `ViewCtg` | View's Catalog | nVarChar | 250 | - |  |  |
| 18 | `ViewSyn` | View's Synonym | nVarChar | 250 | - |  |  |
| 19 | `Viewid` | Query Number | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE | Yes | PackagCode |
