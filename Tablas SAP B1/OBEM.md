# OBEM - SAP Sustainability Footprint Management Footprint Inventory Scope Period

- **Tabla:** OBEM
- **Descripción:** SAP Sustainability Footprint Management Footprint Inventory Scope Period
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBEM.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Period Internal No. | Int | 11 | - |  |  |
| 2 | `ScopeKey` | Footprint Inventory Scope Identifier in PFMCOP | nVarChar | 36 | - |  |  |
| 3 | `ScopeName` | Footprint Inventory Scope Name | nVarChar | 36 | - |  |  |
| 4 | `Periodic` | Periodicity | VarChar | 1 | - | M | `M` = Month<br>`Y` = Year |
| 5 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 6 | `EndDate` | End Date | Date | 8 | - |  |  |
| 7 | `Status` | Status | VarChar | 1 | - | N | `N` = New<br>`I` = Initializing<br>`R` = Reinitializing<br>`P` = In Process<br>`C` = Complete<br>`E` = Error<br>`A` = Complete with Inconsistencies |
| 8 | `UpdateDate` | Last Transactional Data Update Date | Date | 8 | - |  |  |
| 9 | `LastRepId` | Last Replication Identifier | nVarChar | 36 | - |  |  |
| 10 | `RepMessage` | Replication Message | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
