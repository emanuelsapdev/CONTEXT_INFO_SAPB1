# IVLG - Inventory Revaluation Log File

- **Tabla:** IVLG
- **Descripción:** Inventory Revaluation Log File
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IVLG.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Unique Key | Int | 11 | - |  |  |
| 2 | `UtilVer` | Inventory Revaluation Utility | Int | 11 | - |  |  |
| 3 | `B1Ver` | B1 Version | Int | 11 | - |  |  |
| 4 | `SrcDBVer` | Source Database Version | Int | 11 | - |  |  |
| 5 | `DestDBName` | Destination Database Name | nVarChar | 128 | - |  |  |
| 6 | `DestDBPath` | Destination Database Path | Text | 16 | - |  |  |
| 7 | `FromDoc` | Document From | Int | 11 | [OINM](OINM.md) |  |  |
| 8 | `FromSysDat` | System Date From | Date | 8 | - |  |  |
| 9 | `ToDoc` | Last calculated document | Int | 11 | [OINM](OINM.md) |  |  |
| 10 | `ToSysDate` | To System Date | Date | 8 | - |  |  |
| 11 | `CustDbUpd` | Customer DB was updated | VarChar | 1 | - | N | `Y`<br>`N` |
| 12 | `HistTblCrt` | History tables created | VarChar | 1 | - | N | `Y`<br>`N` |
| 13 | `SuccRecalc` | Successful recalculation | VarChar | 1 | - | N | `Y`<br>`N` |
| 14 | `Comment` | Recalculation Comment | nVarChar | 100 | - |  |  |
| 15 | `EnblFromTo` | Enabling From-To Function | VarChar | 1 | - | N |  |
| 16 | `StrFld` | General String Field | nVarChar | 50 | - |  |  |
| 17 | `NumFld` | Include Custom from OIPF | Int | 11 | - |  |  |
| 18 | `LoadCust` | Load Customs on Item Value | VarChar | 1 | - | Y | `Y` = "Load Customs on Item Value" is selected<br>`N` = "Load Customs on Item Value" is not selected |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
