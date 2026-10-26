# AEBK - E-Books - History

- **Tabla:** AEBK
- **Descripción:** E-Books - History
- **Cantidad de campos:** 27
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AEBK.html

## Campos (27)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | E-Books Abs. Entry | Int | 11 | - |  |  |
| 2 | `MARK` | MARK | nVarChar | 40 | - |  |  |
| 3 | `CancelMARK` | Cancel MARK | nVarChar | 40 | - |  |  |
| 4 | `UID` | UID | nVarChar | 50 | - |  |  |
| 5 | `IssueVATID` | Issuer VAT Number | nVarChar | 64 | - |  |  |
| 6 | `CPVATID` | Counterpart VAT Number | nVarChar | 64 | - |  |  |
| 7 | `Series` | Series | nVarChar | 16 | - |  |  |
| 8 | `AA` | AA | nVarChar | 200 | - |  |  |
| 9 | `IssueDate` | Issue Date | Date | 8 | - |  |  |
| 10 | `InvoiceTyp` | Invoice Type | nVarChar | 100 | - |  |  |
| 11 | `Currency` | Currency | nVarChar | 200 | - |  |  |
| 12 | `TlNetVal` | Total Net Value | Num | 19.6 | - |  |  |
| 13 | `TlVatAmn` | Total VAT Amount | Num | 19.6 | - |  |  |
| 14 | `TlWheldAmn` | Total Withheld Amount | Num | 19.6 | - |  |  |
| 15 | `TlGrossVal` | Total Gross Value | Num | 19.6 | - |  |  |
| 16 | `LinkDocTyp` | Linked Doc. Type | Int | 11 | - |  | `18` = A/P Invoices<br>`19` = A/P Credit Memos<br>`30` = Journal Entries<br>`0`<br>`-1` |
| 17 | `LinkDocEnt` | Linked Doc. Entry | Int | 11 | - |  |  |
| 18 | `IsNegMark` | Is Negative MARK | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 19 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 20 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 21 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 22 | `CreateTS` | Create Time - Incl. Secs | Int | 11 | - |  |  |
| 23 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 24 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 25 | `SourceECM8` | LogNum of Source ECM8 | Int | 11 | - |  |  |
| 26 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 234003013 | `234003013` = E-Books Expense |
| 27 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstanc |
| MARK | Yes | MARK, LogInstanc |
