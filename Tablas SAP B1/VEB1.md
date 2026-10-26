# VEB1 - VAT Exemptions for Business Partners Row

- **Tabla:** VEB1
- **Descripción:** VAT Exemptions for Business Partners Row
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/VEB1.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ExmpDoc` | Exemption Doc. No. | nVarChar | 40 | - |  |  |
| 4 | `IssueDate` | Date of Issue | Date | 8 | - |  |  |
| 5 | `IssueTime` | Time of Issue | Int | 11 | - |  |  |
| 6 | `ExmpType` | Exemption Type | Int | 6 | [OVET](OVET.md) |  |  |
| 7 | `AllItems` | Apply to All Items | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 9 | `ItemDesc` | Item Description | nVarChar | 200 | - |  |  |
| 10 | `Rate` | Rate % | Num | 19.6 | - |  |  |
| 11 | `TaxCode` | Exemption Tax Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 12 | `AuthName` | Name of Authorities | nVarChar | 160 | - |  |  |
| 13 | `ValidFrom` | Valid From | Date | 8 | - |  |  |
| 14 | `ValidTo` | Valid To | Date | 8 | - |  |  |
| 15 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 16 | `VisOrder` | Visual Order | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
