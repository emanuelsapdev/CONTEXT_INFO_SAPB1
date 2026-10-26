# RTW2 - Boleto Retorno Wizard: Import Archive

- **Tabla:** RTW2
- **Descripción:** Boleto Retorno Wizard: Import Archive
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RTW2.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Absolute Entry | Int | 11 | - |  |  |
| 2 | `SequenceNo` | Sequence No. | Int | 11 | - |  |  |
| 3 | `StampDate` | Time Stamp Date | Date | 8 | - |  |  |
| 4 | `RetFile` | Retorno File | nVarChar | 254 | - |  |  |
| 5 | `Format` | File Format Name | nVarChar | 100 | - |  |  |
| 6 | `BankCode` | Bank Code | nVarChar | 30 | - |  |  |
| 7 | `Account` | Acct No. | nVarChar | 50 | - |  |  |
| 8 | `RunType` | Run Type | VarChar | 1 | - | D | `D` = Draft<br>`X` = Executed |
| 9 | `RunRecords` | Run Records | Int | 11 | - |  |  |
| 10 | `ImCardName` | Import Card Name | VarChar | 1 | - | N |  |
| 11 | `PostDate` | Posting Date | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
