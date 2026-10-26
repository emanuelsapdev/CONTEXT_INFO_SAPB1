# OEFDW - EFD Wizard

- **Tabla:** OEFDW
- **Descripción:** EFD Wizard
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OEFDW.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `RunName` | Wizard Run Name | nVarChar | 100 | - |  |  |
| 3 | `RunDate` | Wizard Run Date | Date | 8 | - |  |  |
| 4 | `RunTime` | Wizard Run Time | Int | 6 | - |  |  |
| 5 | `Status` | Status | VarChar | 1 | - |  | `S` = Saved<br>`E` = Executed |
| 6 | `UserSign` | User Signature | Int | 11 | [OUSR](OUSR.md) |  |  |
| 7 | `DateFrom` | Date From | Date | 8 | - |  |  |
| 8 | `DateTo` | Date To | Date | 8 | - |  |  |
| 9 | `Branch` | Branch | Int | 11 | [OUBR](OUBR.md) | -2 |  |
| 10 | `ProfType` | Profile Type | nVarChar | 2 | - |  |  |
| 11 | `BlockC` | Block C | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 12 | `BlockD` | Block D | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 13 | `BlockE` | Block E | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 14 | `BlockH` | Block H | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 15 | `BlockG` | Block G | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 16 | `BlockI` | Block I | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 17 | `FlPurCode` | File Purpose Code | VarChar | 1 | - |  | `0` = Remessa do arquivo original<br>`1` = Remessa do arquivo substituto |
| 18 | `AccEmploye` | Accountant Employee | Int | 11 | [OCRD](OCRD.md) |  |  |
| 19 | `AccExtern` | Accountant External | nVarChar | 15 | [OHEM](OHEM.md) |  |  |
| 20 | `ItmFrom` | From Item | nVarChar | 50 | - |  |  |
| 21 | `ItmTo` | To Item | nVarChar | 50 | - |  |  |
| 22 | `ItmGroup` | Item Group | Int | 6 | - |  |  |
| 23 | `ItQryGroup` | Item Properties | nVarChar | 250 | - |  |  |
| 24 | `RptReason` | Reporting Reason | nVarChar | 2 | - | 01 | `01` = No final no per�odo<br>`02` = Na mudan�a de forma de tributa��o da mercadoria (ICMS)<br>`03` = Na solicita��o da baixa cadastral, paralisa��o tempor�ria e outras situa��es<br>`04` = Na altera��o de regime de pagamento � condi��o do contribuinte<br>`05` = Por determina��o dos fiscos |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
