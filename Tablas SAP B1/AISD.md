# AISD - Input Service Distribution

- **Tabla:** AISD
- **Descripción:** Input Service Distribution
- **Cantidad de campos:** 31
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AISD.html

## Campos (31)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 3 | `SrcLctCode` | Source Location Code | Int | 11 | - |  |  |
| 4 | `SrcLctName` | Source Location Name | nVarChar | 100 | - |  |  |
| 5 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 6 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 7 | `DocDate` | Document Date | Date | 8 | - |  |  |
| 8 | `DocStatus` | Document Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Canceled |
| 9 | `Revised` | Revised | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `OrgRefNo` | Original Reference No. | nVarChar | 100 | - |  |  |
| 11 | `OrgRefEty` | Original Reference Entry | Int | 11 | - |  |  |
| 12 | `OrgDocDate` | Original Document Date | Date | 8 | - |  |  |
| 13 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 14 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 15 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 16 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 17 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 18 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 19 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 20 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 21 | `Handwrtten` | Manual Numbering | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 22 | `PIndicator` | Period Indicator | nVarChar | 10 | [OPID](OPID.md) |  |  |
| 23 | `DstPercent` | Percent to Distribute | Num | 19.6 | - |  |  |
| 24 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 25 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |
| 26 | `VATRegNum` | VAT Reg. Number | nVarChar | 32 | - |  |  |
| 27 | `SrcDocType` | Source Document Type | Int | 11 | - |  | `18` = GST Tax Invoice<br>`-19` = GST Debit Memo/GST Credit Memo |
| 28 | `FromNum` | Document Number From | Int | 11 | - |  |  |
| 29 | `ToNum` | Document Number To | Int | 11 | - |  |  |
| 30 | `FromDate` | Document Date From | Date | 8 | - |  |  |
| 31 | `ToDate` | Document Date To | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LogInstanc |
| INDEX | Yes | DocNum, PIndicator, LogInstanc |
