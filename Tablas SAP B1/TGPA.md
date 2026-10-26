# TGPA - Gross Profit Adjustment - Log

- **Tabla:** TGPA
- **Descripción:** Gross Profit Adjustment - Log
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TGPA.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Identity | 11 | - |  |  |
| 2 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 3 | `ItemName` | Item Description | nVarChar | 200 | - |  |  |
| 4 | `LineID` | Line ID | Int | 11 | - |  |  |
| 5 | `Selected` | Selected | VarChar | 1 | - | N |  |
| 6 | `DocType` | Document Type | nVarChar | 20 | - |  |  |
| 7 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 8 | `DocAbs` | Document Abs. Entry | Int | 11 | - |  |  |
| 9 | `DocLineNum` | Document Line Number | Int | 11 | - |  |  |
| 10 | `ManagedBy` | Managed By | Int | 11 | - | -1 | `10000044` = Batch Numbers<br>`10000045` = Serial Numbers |
| 11 | `SysNumber` | System Number | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
