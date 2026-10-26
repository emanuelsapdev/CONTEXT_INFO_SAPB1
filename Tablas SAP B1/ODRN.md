# ODRN - Depreciation Run

- **Tabla:** ODRN
- **Descripción:** Depreciation Run
- **Cantidad de campos:** 23
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODRN.html

## Campos (23)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 3 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 4 | `DprArea` | Depreciation Area ID | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 5 | `Status` | Status | VarChar | 1 | - | D | `S` = Depreciation Posted<br>`N` = No Depreciation Posted<br>`C` = Canceled<br>`F` = Failed<br>`D` |
| 6 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `RefDate` | Posting Date | Date | 8 | - |  |  |
| 8 | `PeriodCat` | Period Category ID | nVarChar | 10 | - |  |  |
| 9 | `PostPeriod` | Posting Subperiod | Int | 11 | - |  |  |
| 10 | `KeyDate` | Key Date | Date | 8 | - |  |  |
| 11 | `Remarks` | Remarks | nVarChar | 32 | - |  |  |
| 12 | `NumOfJEs` | No. of Journal Entries | Int | 11 | - |  |  |
| 13 | `SumOfDpr` | Sum of Depreciation | Num | 19.6 | - |  |  |
| 14 | `SumByPro` | Summarize by Project | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `SumByDistr` | Summarize by Distribution Rule | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `TransType` | Generate Document | nVarChar | 20 | - | -1 | `-1` = None<br>`18` = A/P Invoice |
| 17 | `TransAbs` | Generate Doc. Abs. Entry | Int | 11 | - |  |  |
| 18 | `Handwrtten` | Manual Numbering | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 19 | `BPLId` | Branch | Int | 11 | - |  |  |
| 20 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |
| 21 | `VatRegNum` | VAT Reg. Number | nVarChar | 32 | - |  |  |
| 22 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 23 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Summary<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year of Transfer |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
| NUM | No | DocNum |
