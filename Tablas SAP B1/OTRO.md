# OTRO - Transportation Document

- **Tabla:** OTRO
- **Descripción:** Transportation Document
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTRO.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `NextNum` | Consecutive Number | Int | 11 | - |  |  |
| 3 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 4 | `EDocGenTyp` | Electronic Doc. Generation Type | VarChar | 1 | - | N | `N` = Not Relevant<br>`G` = Generate |
| 5 | `EDocExpFrm` | Electronic Doc. Export Format | Int | 11 | - |  |  |
| 6 | `TranspNum` | Transportation Number | nVarChar | 100 | - |  |  |
| 7 | `Expiration` | Expiration Date | Date | 8 | - |  |  |
| 8 | `Vehicle` | Vehicle ID | nVarChar | 10 | - |  |  |
| 9 | `TrailerID` | Trailer ID | nVarChar | 10 | - |  |  |
| 10 | `Carrier` | Carrier Code | nVarChar | 15 | - |  |  |
| 11 | `IssueGate` | Issue Gate | Int | 11 | - | 0 |  |
| 12 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 13 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 14 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 15 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 16 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 17 | `CreateDate` | Production Date | Date | 8 | - |  |  |
| 18 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 19 | `CANCELED` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `Weight` | Weight | Num | 19.6 | - |  |  |
| 21 | `WghtUnit` | Unit of Weight | Int | 6 | - |  |  |
| 22 | `TotalLC` | Row Total | Num | 19.6 | - |  |  |
| 23 | `WhsCode` | Warehouse Code | nVarChar | 8 | - |  |  |
| 24 | `COTcode` | COT Code | nVarChar | 3 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| NEXT_NUM_U | Yes | NextNum, WhsCode, IssueGate |
