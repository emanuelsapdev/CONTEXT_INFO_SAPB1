# FRC1 - Extend Cat. f. Financial Rep.

- **Tabla:** FRC1
- **Descripción:** Extend Cat. f. Financial Rep.
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FRC1.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CatId` | Numerator | Int | 6 | - |  |  |
| 2 | `TemplateId` | Template | Int | 11 | [OFRT](OFRT.md) |  |  |
| 3 | `AcctCode` | Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 4 | `VisOrder` | Display Order | Int | 6 | - |  |  |
| 5 | `CFWId` | Cash Flow Line Item ID | Int | 11 | [OCFW](OCFW.md) |  |  |
| 6 | `CalcMethod` | Calculation Method | nVarChar | 30 | - |  | `BOP` = Beginning of Period<br>`EOP` = End of Period<br>`CPID` = Current Period In Debit<br>`CPIC` = Current Period In Credit<br>`CPIB` = Current Period In Both |
| 7 | `SlpCode` | Sales Unit Code | Int | 11 | [OSLP](OSLP.md) |  |  |
| 8 | `PrcCode` | Cost Center Code | nVarChar | 8 | [OPRC](OPRC.md) |  |  |
| 9 | `CalMethod2` | Calculation Method 2 | nVarChar | 30 | - |  |  |
| 10 | `CalMethod3` | Calculation Method 3 | nVarChar | 30 | - |  |  |
| 11 | `Linked` | Linked | VarChar | 1 | - | B | `B` = Balance<br>`D` = Debit<br>`C` = Credit |
| 12 | `Sign` | Sign | VarChar | 1 | - | E | `E`<br>`P` = Positive<br>`N` = Negative |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TemplateId, CatId, AcctCode, VisOrder |
| ACCNT_CODE | No | AcctCode |
