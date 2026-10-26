# EBL1 - E-Balance Report Data

- **Tabla:** EBL1
- **Descripción:** E-Balance Report Data
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EBL1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `ReportType` | Report Type | Int | 11 | - | 0 | `0`<br>`1` = E-General Information GCD (Global Common Document)<br>`2` = e-Balance Sheet<br>`3` = e-Profit and Loss<br>`4` = E-Taxable Profit and Loss<br>`5` = E-Income Usage<br>`6` = E-Assets History Sheet<br>`7` = Shareholder<br>`8` = Account Verification<br>`-1` = Global Common Data<br>`-2` = Global Common Report Data |
| 4 | `Selected` | Selected | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `Mandatory` | Mandatory | VarChar | 1 | - |  |  |
| 6 | `DocType` | Document Type | VarChar | 1 | - |  | `0` = XBRL |
| 7 | `DocContent` | Document Content | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
