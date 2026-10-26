# OBNH - Bank Statement Header

- **Tabla:** OBNH
- **Descripción:** Bank Statement Header
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBNH.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IdNumber` | Internal Number | Int | 11 | - |  |  |
| 2 | `ActKey` | Bank Account Internal Number | Int | 11 | [DSC1](DSC1.md) |  |  |
| 3 | `BSNum` | Statement Internal Number | Int | 11 | - |  |  |
| 4 | `BSDate` | Statement Date | Date | 8 | - |  |  |
| 5 | `Status` | Status | VarChar | 1 | - | D | `E` = Finalized<br>`D` = Draft<br>`O` = Old |
| 6 | `Imported` | Imported From File | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 7 | `StrtBlncF` | Starting Balance (FC) | Num | 19.6 | - |  |  |
| 8 | `EndBlncF` | Ending Balance (FC) | Num | 19.6 | - |  |  |
| 9 | `Currency` | Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 10 | `StrtBlncL` | Starting Balance (LC) | Num | 19.6 | - |  |  |
| 11 | `EndBlncL` | Ending Balance (LC) | Num | 19.6 | - |  |  |
| 12 | `FileCRC` | Bank Statement File Hash | nVarChar | 32 | - |  |  |
| 13 | `StmtGuid` | Bank Statement GUID | nVarChar | 32 | - |  |  |
| 14 | `BSFileNum` | Bank Statement Number | nVarChar | 50 | - |  |  |
| 15 | `PeriodAbs` | Period Abs Entry | Int | 11 | - |  |  |
| 16 | `DfltBPL` | Default Branch | Int | 11 | - |  |  |
| 17 | `OrigBSDate` | Original Statement Date | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IdNumber |
| ACT_NUM_DT | Yes | ActKey, BSNum, BSDate |
