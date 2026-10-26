# OSLP - Sales Employee

- **Tabla:** OSLP
- **Descripción:** Sales Employee
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSLP.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SlpCode` | Sales Employee Code | Int | 11 | - |  |  |
| 2 | `SlpName` | Sales Employee Name | nVarChar | 155 | - |  |  |
| 3 | `Memo` | Remarks | nVarChar | 50 | - |  |  |
| 4 | `Commission` | % Commission for Sales Employee | Num | 19.6 | - |  |  |
| 5 | `GroupCode` | Commission Group | Int | 6 | [OCOG](OCOG.md) | 0 |  |
| 6 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 8 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `EmpID` | Employee ID | Int | 11 | [OHEM](OHEM.md) |  |  |
| 10 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Active<br>`N` = Inactive |
| 11 | `Telephone` | Telephone | nVarChar | 50 | - |  |  |
| 12 | `Mobil` | Mobile | nVarChar | 50 | - |  |  |
| 13 | `Fax` | Fax | nVarChar | 50 | - |  |  |
| 14 | `Email` | E-Mail | nVarChar | 100 | - |  |  |
| 15 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased<br>`B` = Blocked<br>`U` = Unblocked |
| 16 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SlpCode |
| SLP_NAME | Yes | SlpName |
| COM_GROUP | No | GroupCode |
