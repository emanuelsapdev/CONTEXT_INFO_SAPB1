# OIRI - Input Service Distribution - Recipient Invoice

- **Tabla:** OIRI
- **Descripción:** Input Service Distribution - Recipient Invoice
- **Cantidad de campos:** 30
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OIRI.html

## Campos (30)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 3 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 4 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 5 | `DocDate` | Document Date | Date | 8 | - |  |  |
| 6 | `DocStatus` | Document Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Canceled |
| 7 | `RefNo` | Reference No. | nVarChar | 100 | - |  |  |
| 8 | `RefEntry` | Reference Entry | Int | 11 | - |  |  |
| 9 | `RefDocDate` | Reference Document Date | Date | 8 | - |  |  |
| 10 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 11 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 12 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 13 | `SrcLoc` | Source Location Code | Int | 11 | - |  |  |
| 14 | `SrcLocName` | Source Location Name | nVarChar | 100 | - |  |  |
| 15 | `SrcGSTIN` | Source Location GSTIN | nVarChar | 15 | - |  |  |
| 16 | `TarLoc` | Target Location Code | Int | 11 | - |  |  |
| 17 | `TarLocName` | Target Location Name | nVarChar | 100 | - |  |  |
| 18 | `TarGSTIN` | Target Location GSTIN | nVarChar | 15 | - |  |  |
| 19 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 20 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 21 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 22 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 23 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 24 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 25 | `JrnlMemo` | Journal Remarks | nVarChar | 254 | - |  |  |
| 26 | `Handwrtten` | Manual Numbering | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 27 | `PIndicator` | Period Indicator | nVarChar | 10 | [OPID](OPID.md) |  |  |
| 28 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 29 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |
| 30 | `VATRegNum` | VAT Reg. Number | nVarChar | 32 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
| INDEX | Yes | DocNum, PIndicator |
