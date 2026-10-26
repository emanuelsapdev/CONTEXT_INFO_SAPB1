# AFAR - Fixed Asset Revaluation

- **Tabla:** AFAR
- **Descripción:** Fixed Asset Revaluation
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AFAR.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 3 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 4 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 5 | `AssetDate` | Asset Value Date | Date | 8 | - |  |  |
| 6 | `Ref` | Reference | nVarChar | 32 | - |  |  |
| 7 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 8 | `JrnlMemo` | Journal Remarks | nVarChar | 254 | - |  |  |
| 9 | `DprArea` | Depreciation Area | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 10 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 11 | `Handwrtten` | Manual Numbering | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `PIndicator` | Period Indicator | nVarChar | 10 | [OPID](OPID.md) |  |  |
| 13 | `DocDate` | Document Date | Date | 8 | - |  |  |
| 14 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 15 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |
| 16 | `VatRegNum` | VAT Reg. Number | nVarChar | 32 | - |  |  |
| 17 | `RevalPerc` | Revaluation Percentage % | Num | 19.6 | - |  |  |
| 18 | `IfrsPsting` | Ifrs posting | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 19 | `PrjSmarz` | Summarize by Project | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `DstRlSmarz` | Summarize by Distribution Rule | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 22 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Summary<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year of Transfer |
| 23 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 24 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LogInstanc |
| INDEX | Yes | DocNum, PIndicator, LogInstanc |
