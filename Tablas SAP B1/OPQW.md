# OPQW - Purchase Quotation Generation: Parameter Sets

- **Tabla:** OPQW
- **Descripción:** Purchase Quotation Generation: Parameter Sets
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPQW.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `SetName` | Set Name | nVarChar | 20 | - |  |  |
| 3 | `SetDesc` | Set Description | nVarChar | 100 | - |  |  |
| 4 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 5 | `ModifyDate` | Last Modified Date | Date | 8 | - |  |  |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `CreatDraft` | Create Drafts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `GroupBy` | Group By | VarChar | 1 | - | B | `B` = Business Partner<br>`I` = Item |
| 9 | `ValidUntil` | Valid Until Date | Date | 8 | - |  |  |
| 10 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 11 | `ReqDate` | Required Date | Date | 8 | - |  |  |
| 12 | `BaseOn` | Base On Type | VarChar | 1 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SET_NAME | Yes | SetName |
