# BEM1 - SAP Sustainability Footprint Management Replication Information

- **Tabla:** BEM1
- **Descripción:** SAP Sustainability Footprint Management Replication Information
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BEM1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Master Data Replication Internal No. | Int | 11 | - |  |  |
| 2 | `MDStatus` | Master Data Replication Status | VarChar | 1 | - | N | `N` = New<br>`I` = Initializing<br>`R` = Reinitializing<br>`P` = In Process<br>`C` = Complete<br>`E` = Error<br>`A` = Complete with Inconsistencies |
| 3 | `UpdMDDate` | Last Update Date of Master Data | Date | 8 | - |  |  |
| 4 | `ScpStatus` | Get Footprint Inventory Scope Import Status | VarChar | 1 | - | N | `N` = New<br>`I` = Initializing<br>`R` = Reinitializing<br>`P` = In Process<br>`C` = Complete<br>`E` = Error<br>`A` = Complete with Inconsistencies |
| 5 | `UpdScpDate` | Last Update Date of Footprint Inventory Scopes Import | Date | 8 | - |  |  |
| 6 | `RepMessage` | Replication Status Message | Text | 16 | - |  |  |
| 7 | `LastRepId` | Master Data Last Replication ID | nVarChar | 36 | - |  |  |
| 8 | `Dimension` | Cost Accounting Dimension | nVarChar | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
