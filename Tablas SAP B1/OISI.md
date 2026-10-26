# OISI - Input Service Distribution - Invoice

- **Tabla:** OISI
- **Descripción:** Input Service Distribution - Invoice
- **Cantidad de campos:** 32
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OISI.html

## Campos (32)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 3 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 4 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 5 | `DocDate` | Document Date | Date | 8 | - |  |  |
| 6 | `DocStatus` | Document Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Canceled |
| 7 | `Revised` | Revised | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `OrgRefNo` | Original Reference No. | nVarChar | 100 | - |  |  |
| 9 | `OrgRefEty` | Original Reference Entry | Int | 11 | - |  |  |
| 10 | `OrgDocDate` | Original Document Date | Date | 8 | - |  |  |
| 11 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 12 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 13 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 14 | `SrcLoc` | Source Location Code | Int | 11 | - |  |  |
| 15 | `SrcLocName` | Source Location Name | nVarChar | 100 | - |  |  |
| 16 | `SrcGSTIN` | Source Location GSTIN | nVarChar | 15 | - |  |  |
| 17 | `TarLoc` | Target Location Code | Int | 11 | - | 0 |  |
| 18 | `TarLocName` | Target Location Name | nVarChar | 100 | - |  |  |
| 19 | `TarGSTIN` | Target Location GSTIN | nVarChar | 15 | - |  |  |
| 20 | `ISDEntry` | ISD Entry | Int | 11 | - |  |  |
| 21 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 22 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 23 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 24 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 25 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 26 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 27 | `JrnlMemo` | Journal Remarks | nVarChar | 254 | - |  |  |
| 28 | `Handwrtten` | Manual Numbering | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 29 | `PIndicator` | Period Indicator | nVarChar | 10 | [OPID](OPID.md) |  |  |
| 30 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 31 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |
| 32 | `VATRegNum` | VAT Reg. Number | nVarChar | 32 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
| INDEX | Yes | DocNum, PIndicator |
