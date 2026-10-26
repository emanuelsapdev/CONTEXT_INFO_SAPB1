# OPR1 - Opportunity - Rows

- **Tabla:** OPR1
- **Descripción:** Opportunity - Rows
- **Cantidad de campos:** 25
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPR1.html

## Campos (25)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `OpprId` | Sequence No. | Int | 11 | [OOPR](OOPR.md) |  |  |
| 2 | `Line` | Row No. | Int | 6 | - |  |  |
| 3 | `SlpCode` | Sales Employee | Int | 11 | [OSLP](OSLP.md) |  |  |
| 4 | `CntctCode` | Contact Person | Int | 11 | [OCPR](OCPR.md) |  |  |
| 5 | `OpenDate` | Start Date | Date | 8 | - |  |  |
| 6 | `CloseDate` | Closing Date | Date | 8 | - |  |  |
| 7 | `Step_Id` | Stage Key | Int | 11 | [OOST](OOST.md) |  |  |
| 8 | `ClosePrcnt` | Percentage Rate | Num | 19.6 | - |  |  |
| 9 | `MaxSumLoc` | Max. Local Total | Num | 19.6 | - |  |  |
| 10 | `MaxSumSys` | Max. System Total | Num | 19.6 | - |  |  |
| 11 | `Memo` | Remarks | Text | 16 | - |  |  |
| 12 | `DocId` | Object Code | Int | 11 | - |  |  |
| 13 | `ObjType` | Object Type | nVarChar | 9 | - | -1 | `-1`<br>`0`<br>`23` = Sales Quotations<br>`17` = Sales Orders<br>`15` = Delivery Notes<br>`13` = Sales Invoices<br>`540000006` = Purchase Quotations<br>`22` = Purchase Orders<br>`20` = Goods Receipt POs<br>`18` = Purchase Invoices |
| 14 | `Status` | Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 15 | `Linked` | Activity | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `WtSumLoc` | Weighted Amount (LC) - Rows | Num | 19.6 | - |  |  |
| 17 | `WtSumSys` | Weighted Amount (SC) | Num | 19.6 | - |  |  |
| 18 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 19 | `ChnCrdCode` | BP Channel Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 20 | `ChnCrdName` | BP Channel Name | nVarChar | 200 | - |  |  |
| 21 | `ChnCrdCon` | BP Channel Contact | Int | 11 | [OCPR](OCPR.md) |  |  |
| 22 | `DocChkbox` | Document Checkbox | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 23 | `Owner` | Data Ownership Field | Int | 11 | [OHEM](OHEM.md) |  |  |
| 24 | `DocNumber` | Document Number | Int | 11 | - |  |  |
| 25 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | OpprId, Line |
