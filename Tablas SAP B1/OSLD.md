# OSLD - Schedule Row Detail

- **Tabla:** OSLD
- **Descripción:** Schedule Row Detail
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSLD.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ObjType` | Object Type | nVarChar | 20 | - | -1 | `-1`<br>`13` = A/R Reserve Invoice<br>`17` = Sales Order<br>`18` = A/P Reserve Invoice<br>`22` = Purchase Order<br>`163` = A/P Correction Reserve Invoice<br>`165` = A/R Correction Reserve Invoice<br>`202` = Production Order<br>`1250000001` = Warehouse Transfer Request |
| 3 | `DocEntry` | Associated Doc Entry | Int | 11 | - |  |  |
| 4 | `DocLineNum` | Associated Doc Row No. | Int | 11 | - |  |  |
| 5 | `SchdLine` | Schedule Row No. | Int | 11 | - |  |  |
| 6 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 7 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 8 | `CfmDate` | Confirmation Date | Date | 8 | - |  |  |
| 9 | `CfmQty` | Confirmation Quantity | Num | 19.6 | - |  |  |
| 10 | `FixedCfm` | Fixed Confirmation Data | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `ReqQty` | Required Quantity | Num | 19.6 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SCHD_LINE | Yes | ObjType, DocEntry, DocLineNum, SchdLine |
| DOCLINESLD | No | ObjType, DocEntry, DocLineNum |
