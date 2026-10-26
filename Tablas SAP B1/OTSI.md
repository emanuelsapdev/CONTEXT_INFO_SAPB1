# OTSI - Sales Tax Invoice

- **Tabla:** OTSI
- **Descripción:** Sales Tax Invoice
- **Cantidad de campos:** 47
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTSI.html

## Campos (47)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 3 | `DocType` | Document Type | VarChar | 1 | - | I | `I` = Invoice<br>`P` = Payment<br>`J` = Journal Entry<br>`C` = Correction Invoice<br>`A` = Alteration Invoice<br>`B` = Alteration Correction Invoice |
| 4 | `CANCELED` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `HandWriten` | Manual Numbering | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `Printed` | Printed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `Transfered` | Year Transfer | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 194 |  |
| 9 | `DocDate` | Posting Date | Date | 8 | - |  |  |
| 10 | `CardCode` | Customer Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 11 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 12 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 13 | `DocDueDate` | Due Date | Date | 8 | - |  |  |
| 14 | `Series` | Series | Int | 11 | - | 0 |  |
| 15 | `Segment` | Segment | Int | 6 | - | 0 |  |
| 16 | `CntctCode` | Contact Person | Int | 11 | [OCPR](OCPR.md) |  |  |
| 17 | `VatDate` | Document Date | Date | 8 | - |  |  |
| 18 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 19 | `TrnspCode` | Shipping Type | Int | 6 | [OSHP](OSHP.md) | -1 |  |
| 20 | `ShipToCode` | Ship-to Code | nVarChar | 50 | - |  |  |
| 21 | `Address` | Bill To | nVarChar | 254 | - |  |  |
| 22 | `Address2` | Ship To | nVarChar | 254 | - |  |  |
| 23 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 24 | `CurSource` | Base Currency | VarChar | 1 | - | C | `L` = Local Currency<br>`S` = System Currency<br>`C` = BP Currency |
| 25 | `DocCur` | Document Currency | nVarChar | 3 | - |  |  |
| 26 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 27 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 28 | `NumAtCard` | BP Reference No. | nVarChar | 200 | - |  |  |
| 29 | `CardName` | Customer/Vendor Name | nVarChar | 200 | - |  |  |
| 30 | `CancelDate` | Cancel Date | Date | 8 | - |  |  |
| 31 | `DocTotal` | Document Total | Num | 19.6 | - |  |  |
| 32 | `VatSum` | Total Tax | Num | 19.6 | - |  |  |
| 33 | `PayRefNo` | Payment Ref. No. | nVarChar | 16 | - |  |  |
| 34 | `PayRefDate` | Payment Ref. No. Date | Date | 8 | - |  |  |
| 35 | `TaxMethod` | Taxation Method | VarChar | 1 | - | S | `S` = On Shipment<br>`P` = On Payment |
| 36 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 37 | `IsDpm` | IS Down Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 38 | `AltRev` | Alteration Revision | Int | 11 | - | 0 |  |
| 39 | `PIndicator` | Period Indicator | nVarChar | 10 | [OPID](OPID.md) |  |  |
| 40 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 41 | `JrnlMemo` | Journal Remark | nVarChar | 254 | - |  |  |
| 42 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 43 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |
| 44 | `VATRegNum` | Branch Reg. No. | nVarChar | 32 | - |  |  |
| 45 | `GovContrID` | Gov. Contract ID | nVarChar | 254 | - |  |  |
| 46 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 47 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
| NUM | Yes | DocNum, AltRev, PIndicator, Series |
