# APKL - Pick List - History

- **Tabla:** APKL
- **Descripción:** Pick List - History
- **Cantidad de campos:** 22
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/APKL.html

## Campos (22)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Absolute entry | Int | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 155 | - |  |  |
| 3 | `OwnerCode` | Owner Code | Int | 6 | [OUSR](OUSR.md) |  |  |
| 4 | `OwnerName` | Owner Name | nVarChar | 155 | - |  |  |
| 5 | `PickDate` | Pick Date | Date | 8 | - |  |  |
| 6 | `Remarks` | Remarks | Text | 16 | - |  |  |
| 7 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `ShipType` | Shipping Type | Int | 6 | - |  |  |
| 9 | `Status` | Status | VarChar | 1 | - | R | `R` = Released<br>`Y` = Picked<br>`P` = Partially Picked<br>`D` = Partially Delivered<br>`C` = Closed |
| 10 | `Printed` | Printed | VarChar | 1 | - | N | `Y` = Copy<br>`N` = Original |
| 11 | `LogInstac` | Log Instance - History | Int | 11 | - |  |  |
| 12 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 156 |  |
| 13 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 14 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 15 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 16 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 17 | `UseBaseUn` | Inventory UoM | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `QRCodeSrc` | QR Code Source | Text | 16 | - |  |  |
| 19 | `QRCodeSPGn` | QR Code Source Generated from Stored Procedure | Text | 16 | - |  |  |
| 20 | `CreateTS` | Create Time Incl. Secs. | Int | 11 | - |  |  |
| 21 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 22 | `DocSubType` | Document Subtype | nVarChar | 2 | - | -- | `--` = Pick List |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstac |
