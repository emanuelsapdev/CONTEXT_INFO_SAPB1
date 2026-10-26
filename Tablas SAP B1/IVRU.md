# IVRU - Inventory Valuation Utility

- **Tabla:** IVRU
- **Descripción:** Inventory Valuation Utility
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IVRU.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Successive No. | Int | 11 | - |  |  |
| 2 | `SourceDB` | Source Database | nVarChar | 128 | - |  |  |
| 3 | `UtilityDB` | Utility DB | nVarChar | 128 | - |  |  |
| 4 | `IVLGEntry` | IVLG Entry | Int | 11 | [IVLG](IVLG.md) |  |  |
| 5 | `UpdDate` | Update Date and Time | Date | 8 | - |  |  |
| 6 | `TblHINM` | HINM Name | nVarChar | 30 | - |  |  |
| 7 | `TblHITM` | HITM Name | nVarChar | 30 | - |  |  |
| 8 | `TblHITW` | HITW Name | nVarChar | 30 | - |  |  |
| 9 | `TblFINM` | FINM Name | nVarChar | 30 | - |  |  |
| 10 | `TblFITM` | FITM Name | nVarChar | 30 | - |  |  |
| 11 | `TblFITW` | FITW Name | nVarChar | 30 | - |  |  |
| 12 | `TrSeqHINM` | Last HINM Trans. Seq. No. | Int | 11 | - |  |  |
| 13 | `TrSeqOINM` | Last OINM Trans. Seq. No. | Int | 11 | - |  |  |
| 14 | `TrIdUtil` | Last OJDT Trans. No. Utility | Int | 11 | - |  |  |
| 15 | `TrIdProd` | Last OJDT Trans. No. Productiv | Int | 11 | - |  |  |
| 16 | `Comment` | Comment | nVarChar | 100 | - |  |  |
| 17 | `StrFld` | General String Field | nVarChar | 50 | - |  |  |
| 18 | `NumFld` | General Number Field | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
