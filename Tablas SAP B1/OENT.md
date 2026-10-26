# OENT - Shipping Types

- **Tabla:** OENT
- **Descripción:** Shipping Types
- **Cantidad de campos:** 40
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OENT.html

## Campos (40)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | [OUSR](OUSR.md) |  |  |
| 3 | `BaseDocNum` | Base Document Number | Int | 11 | [OUSR](OUSR.md) |  |  |
| 4 | `Printed` | Printed | VarChar | 1 | - | N | `Y` = Copy<br>`N` = Original |
| 5 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) |  |  |
| 6 | `DocDate` | Posting Date | Date | 8 | - |  |  |
| 7 | `DocDueDate` | Due Date | Date | 8 | - |  |  |
| 8 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 9 | `CardName` | BP Name | nVarChar | 200 | - |  |  |
| 10 | `FreZoneNum` | ID Number | nVarChar | 8 | - |  |  |
| 11 | `Shiper` | Sender | nVarChar | 100 | - |  |  |
| 12 | `Address` | Address | nVarChar | 254 | - |  |  |
| 13 | `FromCntry` | Country/Region - Origin | nVarChar | 100 | - |  |  |
| 14 | `ToCntry` | Country/Region - Destination | nVarChar | 100 | - |  |  |
| 15 | `FromPort` | Origin Port | nVarChar | 100 | - |  |  |
| 16 | `ToPort` | Destination Port | nVarChar | 100 | - |  |  |
| 17 | `AirPlane` | Ship/Aircraft | nVarChar | 50 | - |  |  |
| 18 | `AirPlanNum` | No. of Ships/Aircraft | nVarChar | 40 | - |  |  |
| 19 | `TotalFob` | Total | Num | 19.6 | - |  |  |
| 20 | `Taxes` | Taxes | Num | 19.6 | - |  |  |
| 21 | `Insurance` | Insurance | Num | 19.6 | - |  |  |
| 22 | `Others` | Other | Num | 19.6 | - |  |  |
| 23 | `TotalCif` | Document Total | Num | 19.6 | - |  |  |
| 24 | `Ref1` | Reference 1 | nVarChar | 11 | - |  |  |
| 25 | `Ref2` | Reference 2 | nVarChar | 11 | - |  |  |
| 26 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 27 | `GroupNum` | Payment Terms Code | Int | 6 | [OCTG](OCTG.md) |  |  |
| 28 | `DocTime` | Document Time | Int | 6 | - |  |  |
| 29 | `SlpCode` | Sales Employee | Int | 11 | [OSLP](OSLP.md) | -1 |  |
| 30 | `TrnspCode` | Delivery Code | Int | 6 | [OSHP](OSHP.md) | -1 |  |
| 31 | `PartSupply` | Delivery of Goods | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 32 | `ImportEnt` | Landed Costs | Int | 11 | [OIPF](OIPF.md) |  |  |
| 33 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 34 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 35 | `NumForPrn` | Base Doc. No. for Printing | nVarChar | 100 | [OUSR](OUSR.md) |  |  |
| 36 | `PurPackMsr` | Packaging UoM Name | nVarChar | 8 | - |  |  |
| 37 | `Series` | Series | Int | 11 | - |  |  |
| 38 | `BaseDocObj` | Base Document Object Type | Int | 6 | - |  |  |
| 39 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 40 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (5)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
| NUM | No | DocNum |
| BASE_DOC | No | BaseDocNum, BaseDocObj |
| OBJECT | No | ObjType |
| SERIES | No | Series |
