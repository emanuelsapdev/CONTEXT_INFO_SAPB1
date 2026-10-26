# APFS - Personal Fields Setup - History

- **Tabla:** APFS
- **Descripción:** Personal Fields Setup - History
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/APFS.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `TableName` | Data Subtype | nVarChar | 21 | - |  |  |
| 3 | `FieldName` | Field Name | nVarChar | 50 | - |  |  |
| 4 | `RefObjType` | Data Type | nVarChar | 20 | - |  |  |
| 5 | `Category` | Category | VarChar | 1 | - | N | `N`<br>`R` = Sales A/R<br>`P` = Purchase A/P<br>`Q` = Purchase Request<br>`A` = Inventory Transfers and Requests Sales A/R<br>`B` = Inventory Transfers and Requests Purchase A/P<br>`C` = Opportunity - Business Partner<br>`D` = Opportunity - Business Partner Channel<br>`E` = Customer Equipment Card - Business Partner<br>`F` = Customer Equipment Card - Direct Partner<br>`L` = Landed Cost - Vendor<br>`G` = Landed Cost - Broker<br>`X` = Payment Results - Business Partner<br>`U` = Payment Results - User<br>`H` = Incoming Payments<br>`I` = Outgoing Payments<br>`J` = Sales A/R<br>`K` = Purchase A/P<br>`M` = Bill of Exchange for Incoming Payments<br>`S` = Business Partner - Contact Person<br>`O` = Company<br>`Y` = Service Call - Employee |
| 6 | `OrigType` | Default Data Classification | VarChar | 1 | - | U | `U` = User Defined<br>`S` = Sensitive Personal<br>`P` = Personal<br>`N` = Not Personal |
| 7 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 8 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 9 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 10 | `CreateTS` | Create Time - Incl. Secs | Int | 11 | - |  |  |
| 11 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 12 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 13 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 14 | `Type` | Data Classification | VarChar | 1 | - | N | `N` = Not Personal<br>`S` = Sensitive Personal<br>`P` = Personal |
| 15 | `Descr` | Description | nVarChar | 254 | - |  |  |
| 16 | `MaxType` | Max. Data Classification | VarChar | 1 | - | U | `U` = User Defined<br>`S` = Sensitive Personal<br>`P` = Personal |
| 17 | `SysDefined` | Is System Defined | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstanc |
| SECONDARY | Yes | TableName, FieldName, Category, LogInstanc |
