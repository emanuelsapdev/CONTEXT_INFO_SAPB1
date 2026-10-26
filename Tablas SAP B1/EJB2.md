# EJB2 - Docs List for ERV-JAb Wizard

- **Tabla:** EJB2
- **Descripción:** Docs List for ERV-JAb Wizard
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EJB2.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardID` | Wizard ID | Int | 11 | [OEJB](OEJB.md) |  |  |
| 2 | `DocID` | Document ID | Int | 11 | - |  |  |
| 3 | `Selected` | Selected | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 4 | `Mandatory` | Mandatory | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `Type` | Type | nVarChar | 3 | - |  | `XML` = XML<br>`PDF` = PDF |
| 6 | `RptSec` | Report Section | Int | 11 | - | 0 | `0`<br>`1` = General Information for ERV-JAb<br>`2` = Names of Signatories:<br>`3` = Legal Size Classification<br>`4` = Extract from Balance Sheet (UGB Form 2)<br>`5` = Balance Sheet<br>`6` = P&L Statement<br>`7` = Annex To Be Published (UGB Form 3)<br>`8` = General and Other Explanations<br>`9` = Annex to Balance Sheet Entry<br>`10` = Annex to P&L Statement<br>`11` = Annual Report<br>`12` = Suggestion for Financial Statement Usage<br>`13` = Decision About Financial Statement Usage<br>`14` = Note of Confirmation<br>`15` = Supervisory Board Report<br>`16` = External Auditor Report Acc. to Art. 44 Para. 3 EStG (Income Tax Act)<br>`17` = Finance-Specific Annex<br>`18` = Assets History Sheet<br>`19` = Liabilities History Sheet |
| 7 | `FilePath` | File Path | nVarChar | 254 | - |  |  |
| 8 | `FileStorag` | File Storage | Text | 16 | - |  |  |
| 9 | `VisOrder` | Visual Order | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardID, DocID |
