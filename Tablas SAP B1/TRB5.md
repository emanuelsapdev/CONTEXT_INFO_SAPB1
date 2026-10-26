# TRB5 - Tax Report Wizard Reported Tax Sums

- **Tabla:** TRB5
- **Descripción:** Tax Report Wizard Reported Tax Sums
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TRB5.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OTRB](OTRB.md) |  |  |
| 2 | `State` | State Code | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 3 | `CardCode` | Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 4 | `TransCrdt` | Transferred Credit | Num | 19.6 | - |  |  |
| 5 | `TotalDbt` | Total Reported Debit | Num | 19.6 | - |  |  |
| 6 | `TtlDbtSc` | Total Reported Debit SC | Num | 19.6 | - |  |  |
| 7 | `TotalCrdt` | Total Reported Credit | Num | 19.6 | - |  |  |
| 8 | `TtlCrdtSc` | Total Reported Credit SC | Num | 19.6 | - |  |  |
| 9 | `TotalDed` | Total Reported Tax Deductions | Num | 19.6 | - |  |  |
| 10 | `TtlDedSc` | Total Reported Tax Deductions SC | Num | 19.6 | - |  |  |
| 11 | `BlncDue` | Balance Due | Num | 19.6 | - |  |  |
| 12 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, State |
