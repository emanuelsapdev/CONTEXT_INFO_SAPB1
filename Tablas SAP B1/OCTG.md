# OCTG - Payment Terms

- **Tabla:** OCTG
- **Descripción:** Payment Terms
- **Cantidad de campos:** 31
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCTG.html

## Campos (31)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `GroupNum` | Group Number | Int | 6 | - |  |  |
| 2 | `PymntGroup` | Payment Terms Code | nVarChar | 100 | - |  |  |
| 3 | `PayDuMonth` | Start From | VarChar | 1 | - | N | `E` = Month End<br>`H` = Half Month<br>`Y` = Month Start<br>`N` = Selected Date |
| 4 | `ExtraMonth` | Number of Additional Months | Int | 6 | - | 0 |  |
| 5 | `ExtraDays` | Number of Additional Days | Int | 6 | - | 0 |  |
| 6 | `PaymntsNum` | Number of Payments | Int | 6 | - |  |  |
| 7 | `CredLimit` | Max. Credit | Num | 19.6 | - |  |  |
| 8 | `VolumDscnt` | Total Discount % | Num | 19.6 | - |  |  |
| 9 | `LatePyChrg` | Interest % on Receivables | Num | 19.6 | - |  |  |
| 10 | `ObligLimit` | Commitment Limit | Num | 19.6 | - |  |  |
| 11 | `ListNum` | Price List | Int | 6 | [OPLN](OPLN.md) |  |  |
| 12 | `Payments` | Partial Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `NumOfPmnts` | Number of Payments | Int | 6 | - | 1 |  |
| 14 | `Payment1` | First Partial Payment | Num | 19.6 | - |  |  |
| 15 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 16 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 17 | `OpenRcpt` | Open Incoming Payment | VarChar | 1 | - | N | `N` = No<br>`3` = Cash<br>`1` = Checks<br>`4` = Credit<br>`2` = Bank Transfer<br>`5` = Bill of Exchange |
| 18 | `DiscCode` | Discount Code | nVarChar | 20 | [OCDC](OCDC.md) |  |  |
| 19 | `DunningCod` | Dunning Code | nVarChar | 20 | [ORIT](ORIT.md) |  |  |
| 20 | `BslineDate` | Due Date Based on | VarChar | 1 | - | T | `P` = Posting Date<br>`S` = System Date<br>`T` = Document Date<br>`C` = Closing Date |
| 21 | `InstNum` | No. of Installments | Int | 6 | - |  |  |
| 22 | `TolDays` | No. of Tolerance Days | Int | 6 | - |  |  |
| 23 | `VATFirst` | Apply Tax on 1st Installment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No<br>`T` = Tax Only |
| 24 | `CrdMthd` | Credit Method | VarChar | 1 | - | L | `F` = First Installment<br>`L` = Last Installment<br>`E` = Equally |
| 25 | `CshRelev` | Cash Relevant Transaction | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 26 | `UserSign2` | Update User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 27 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 28 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 29 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 30 | `PDueMonEnd` | End On | VarChar | 1 | - | N | `E` = End of Month<br>`H` = Middle of Month<br>`Y` = Start of Month<br>`N` = None |
| 31 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | GroupNum |
| ABS_ENTRY | Yes | PymntGroup |
