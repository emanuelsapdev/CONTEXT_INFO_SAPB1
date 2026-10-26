# OCTT - Contract Template

- **Tabla:** OCTT
- **Descripción:** Contract Template
- **Cantidad de campos:** 42
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCTT.html

## Campos (42)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TmpltName` | Template Name | nVarChar | 20 | - |  |  |
| 2 | `Deleted` | Deleted | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 3 | `Renewal` | Renewal | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `RemindVal` | Remind Before Renewal | Int | 6 | - |  |  |
| 5 | `RemindUnit` | Remind Unit | VarChar | 1 | - | D | `D` = Day(s)<br>`W` = Week(s)<br>`M` = Month(s) |
| 6 | `Duration` | Duration of Coverage | Int | 6 | - |  |  |
| 7 | `ResponsVal` | Resolution Value | Int | 6 | - |  |  |
| 8 | `ResponsUnt` | Resolution Unit | VarChar | 1 | - | D | `D` = Day(s)<br>`H` = Hour(s) |
| 9 | `Descriptio` | Description | nVarChar | 254 | - |  |  |
| 10 | `PriceList` | Price List No. | Int | 6 | - |  |  |
| 11 | `CntrctType` | Contract Type | VarChar | 1 | - | S | `C` = Customer<br>`G` = Item Group<br>`S` = Serial Number |
| 12 | `MonEnabled` | Monday Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 13 | `TueEnabled` | Tuesday Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 14 | `WedEnabled` | Wednesday Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 15 | `ThuEnabled` | Thursday Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 16 | `FriEnabled` | Friday Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 17 | `SatEnabled` | Saturday Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 18 | `SunEnabled` | Sunday Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 19 | `MonStart` | Monday Start | Int | 6 | - | 800 |  |
| 20 | `MonEnd` | Monday End | Int | 6 | - | 1700 |  |
| 21 | `TueStart` | Tuesday Start | Int | 6 | - | 800 |  |
| 22 | `TueEnd` | Tuesday End | Int | 6 | - | 1700 |  |
| 23 | `WedStart` | Wednesday Start | Int | 6 | - | 800 |  |
| 24 | `WedEnd` | Wednesday End | Int | 6 | - | 1700 |  |
| 25 | `ThuStart` | Thursday Start | Int | 6 | - | 800 |  |
| 26 | `ThuEnd` | Thursday End | Int | 6 | - | 1700 |  |
| 27 | `FriStart` | Friday Start | Int | 6 | - | 800 |  |
| 28 | `FriEnd` | Friday End | Int | 6 | - | 1700 |  |
| 29 | `SatStart` | Saturday Start | Int | 6 | - | 0 |  |
| 30 | `SatEnd` | Saturday End | Int | 6 | - | 2359 |  |
| 31 | `SunStrart` | Sunday Start | Int | 6 | - | 0 |  |
| 32 | `SunEnd` | Sunday End | Int | 6 | - | 2359 |  |
| 33 | `InclParts` | Include Parts | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 34 | `InclWork` | Include Labor | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 35 | `InclTravel` | Include Travel | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 36 | `Attachment` | Attachments | Text | 16 | - |  |  |
| 37 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 38 | `Remark` | Remarks | Text | 16 | - |  |  |
| 39 | `InclHldays` | Include Holidays | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 40 | `ResponseV` | Response Value | Int | 6 | - |  |  |
| 41 | `ResponseU` | Response Unit | VarChar | 1 | - | H | `H` = Hour(s)<br>`D` = Day(s) |
| 42 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TmpltName |
