# ODPL - Link between document lines and pick lists

- **Tabla:** ODPL
- **Descripción:** Link between document lines and pick lists
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODPL.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocType` | Document Type | nVarChar | 20 | - |  |  |
| 3 | `DocEntry` | Document Entry | Int | 11 | - |  |  |
| 4 | `DocLineNum` | Document Row Number | Int | 11 | - |  |  |
| 5 | `PKLEntry` | Pick List Entry | Int | 11 | - |  |  |
| 6 | `PKL1Num` | Row Num of PKL1 | Int | 11 | - |  |  |
| 7 | `PKL2Num` | Row Num of PKL2 | Int | 11 | - | -1 |  |
| 8 | `ItemCode` | Item No. | nVarChar | 50 | - |  |  |
| 9 | `ManagedBy` | Management Method | Int | 11 | - | -1 | `10000044` = BTN<br>`10000045` = SRN<br>`-1` = NOB |
| 10 | `SnBEntry` | SnB Abs. Entry | Int | 11 | - |  |  |
| 11 | `BinAbs` | Bin Internal Number | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| DOC_ENTRY | No | DocEntry |
