# PWZ5 - Payment Wizard - Rows 5

- **Tabla:** PWZ5
- **Descripción:** Payment Wizard - Rows 5
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PWZ5.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IdEntry` | ID Entry | Int | 11 | [OPWZ](OPWZ.md) |  |  |
| 2 | `InvID` | Inv ID | Int | 11 | - |  |  |
| 3 | `Amount` | Invoice Amount | Num | 19.6 | - |  |  |
| 4 | `CardCode` | Card Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 5 | `CardName` | Card Name | nVarChar | 200 | - |  |  |
| 6 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 7 | `ErrDisc` | Error Discription | nVarChar | 254 | - |  |  |
| 8 | `ErrorLine` | ErrorLine | Int | 11 | - |  |  |
| 9 | `WriteErr` | WriteErr | VarChar | 1 | - | Y |  |
| 10 | `Object` | Object Type | nVarChar | 20 | - | 0 |  |
| 11 | `InstlmntID` | Installment ID | Int | 6 | - | 1 |  |
| 12 | `invNum` | Invoice No. | Int | 11 | - |  |  |
| 13 | `Currency` | Currency | nVarChar | 3 | - |  |  |
| 14 | `LineType` | Line Type | VarChar | 1 | - | G |  |
| 15 | `DueBal` | Balance Due | Num | 19.6 | - |  |  |
| 16 | `DueBalFC` | Balance Due (FC) | Num | 19.6 | - |  |  |
| 17 | `DueBalSys` | Balance Due (SC) | Num | 19.6 | - |  |  |
| 18 | `ValDate` | Due Date | Date | 8 | - |  |  |
| 19 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 20 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IdEntry, InvID, ErrorLine, Object, InstlmntID |
