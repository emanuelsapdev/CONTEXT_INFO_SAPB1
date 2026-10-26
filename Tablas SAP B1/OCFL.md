# OCFL - Cash Flow Additional Trans.

- **Tabla:** OCFL
- **Descripción:** Cash Flow Additional Trans.
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCFL.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | Int | 11 | - |  |  |
| 2 | `DateID` | Date | Date | 8 | - |  |  |
| 3 | `Dscription` | Description | nVarChar | 50 | - |  |  |
| 4 | `Project` | Project Code | nVarChar | 20 | - |  |  |
| 5 | `Credit` | Incoming Total | Num | 19.6 | - |  |  |
| 6 | `CredCur` | Entrance Currency | nVarChar | 3 | - |  |  |
| 7 | `Debit` | Outgoing Amount | Num | 19.6 | - |  |  |
| 8 | `DebCur` | Issue Currency | nVarChar | 3 | - |  |  |
| 9 | `SecLevel` | Security Level | Int | 6 | - | 1 | `1` = Cash Account<br>`5` = Credit<br>`2` = Checks<br>`3` = Customer Liabilities<br>`6` = Bill of Exchange<br>`4` = Payable to Vendors<br>`7` = Customer Forecast<br>`8` = Vendor Forecast |
| 10 | `UserId` | User ID | Int | 6 | - |  |  |
| 11 | `Frequency` | Frequency | VarChar | 1 | - | O | `D` = Daily<br>`W` = Weekly<br>`M` = Monthly<br>`Q` = Quarterly<br>`S` = Semiannually<br>`A` = Annually<br>`O` = One Time |
| 12 | `Remind` | Subfrequency | Int | 6 | - | -1 | `-1`<br>`1` = On Sunday<br>`2` = On Monday<br>`3` = On Tuesday<br>`4` = On Wednesday<br>`5` = On Thursday<br>`6` = On Friday<br>`7` = On Saturday<br>`101` = Every 1<br>`102` = Every 2<br>`103` = Every 3<br>`104` = Every 4<br>`105` = Every 5<br>`106` = Every 6<br>`107` = Every 7<br>`108` = Every 8<br>`109` = Every 9<br>`110` = Every 10<br>`115` = Every 15<br>`130` = Every 30<br>`145` = Every 45<br>`160` = Every 60<br>`1001` = On 1<br>`1002` = On 2<br>`1003` = On 3<br>`1004` = On 4<br>`1005` = On 5<br>`1006` = On 6<br>`1007` = On 7<br>`1008` = On 8<br>`1009` = On 9<br>`1010` = On 10<br>`1011` = On 11<br>`1012` = On 12<br>`1013` = On 13<br>`1014` = On 14<br>`1015` = On 15<br>`1016` = On 16<br>`1017` = On 17<br>`1018` = On 18<br>`1019` = On 19<br>`1020` = On 20<br>`1021` = On 21<br>`1022` = On 22<br>`1023` = On 23<br>`1024` = On 24<br>`1025` = On 25<br>`1026` = On 26<br>`1027` = On 27<br>`1028` = On 28<br>`1029` = On 29<br>`1030` = On 30<br>`1031` = On 31 |
| 13 | `EndDate` | Execution End Date | Date | 8 | - |  |  |
| 14 | `OcrCode` | Distribution Rule 1 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 15 | `OcrCode2` | Distribution Rule 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 16 | `OcrCode3` | Distribution Rule 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 17 | `OcrCode4` | Distribution Rule 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 18 | `OcrCode5` | Distribution Rule 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, UserId |
