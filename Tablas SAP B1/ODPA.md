# ODPA - Fixed Asset Depreciation Areas

- **Tabla:** ODPA
- **Descripción:** Fixed Asset Depreciation Areas
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODPA.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 15 | - |  |  |
| 2 | `Descr` | Description | nVarChar | 100 | - |  |  |
| 3 | `DirectDpr` | Direct Depreciation | VarChar | 1 | - | D | `D` = Direct Posting<br>`I` = Indirect Posting |
| 4 | `RetMeth` | Retirement Method | VarChar | 1 | - | G | `G` = Gross<br>`N` = Net |
| 5 | `AreaType` | Area Type | VarChar | 1 | - | O | `L` = Posting to G/L<br>`O` = Additional Area<br>`D` = Derived Area |
| 6 | `DrvdArea` | Derived Area | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 7 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 8 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 10 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 11 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 12 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 13 | `MainArea` | Main Booking Area | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `CreditCtrl` | Tax Credit Control | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `TaxType` | Tax Type | Int | 11 | [OSTT](OSTT.md) |  |  |
| 16 | `DirRevPost` | Direct Revenue Posting | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 17 | `SnapshotId` | Snapshot ID | Int | 11 | - | 0 |  |
| 18 | `BpTaxCorr` | BP for Tax Correction | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 19 | `ItmTaxCorr` | Item for Tax Correction | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 20 | `UsgTaxCorr` | Usage for Tax Correction | Int | 11 | [OUSG](OUSG.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
