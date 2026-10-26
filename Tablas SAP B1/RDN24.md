# RDN24 - Returns - Tracking Note Assignment

- **Tabla:** RDN24
- **Descripción:** Returns - Tracking Note Assignment
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RDN24.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | ODOC |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ChildNum` | Assignment Line | Int | 11 | - |  |  |
| 4 | `TrackingNt` | CCD Tracking Note | Int | 11 | [OTCN](OTCN.md) |  |  |
| 5 | `TrackiNtLn` | CCD Tracking Note Line | Int | 11 | - |  |  |
| 6 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 7 | `ItemCCDNum` | Item CCD Number | nVarChar | 40 | - |  |  |
| 8 | `CntrOrigin` | Country/Region of Origin | nVarChar | 3 | - |  |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 10 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 16 |  |
| 11 | `SubLineNum` | BOM Line No. | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, ChildNum |
