# OGDP - General Data Protection Wizard

- **Tabla:** OGDP
- **Descripción:** General Data Protection Wizard
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OGDP.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `RunName` | Wizard Run Name | nVarChar | 100 | - |  |  |
| 3 | `RunDate` | Wizard Run Date | Date | 8 | - |  |  |
| 4 | `Status` | Wizard Run Status | VarChar | 1 | - | S | `S` = Saved<br>`E` = Executed<br>`P` = Printed<br>`V` = Print Preview Generated |
| 5 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 6 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 7 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 8 | `CreateTS` | Create Time - Incl. Secs | Int | 11 | - |  |  |
| 9 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 10 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 11 | `Action` | Personal Data Management Wizard Action | VarChar | 1 | - | R | `R` = Personal Data Report<br>`E` = Personal Data Cleanup<br>`B` = Personal Data Blocking<br>`U` = Personal Data Unblocking<br>`I` = Determine Natural Persons<br>`N` = Reverse Natural Person Determination |
| 12 | `BPType` | Business Partner Type | VarChar | 1 | - | B | `B` = Business Partners<br>`D` = Default Customers |
| 13 | `PostDateTo` | Posting Date To | Date | 8 | - |  |  |
| 14 | `EmpType` | Employee Type | VarChar | 1 | - | E | `E` = Employees<br>`S` = Sales Employees and Buyers |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SECONDARY | Yes | RunName |
