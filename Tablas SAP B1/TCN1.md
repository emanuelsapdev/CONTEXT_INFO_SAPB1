# TCN1 - Tracking Note - Line Data

- **Tabla:** TCN1
- **Descripción:** Tracking Note - Line Data
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TCN1.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Abs. Entry | Int | 11 | [OTCN](OTCN.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ItemCCDNum` | Item CCD Number | nVarChar | 20 | - |  |  |
| 4 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 5 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 6 | `CntrOrigin` | Country/Region of Origin | nVarChar | 3 | - |  |  |
| 7 | `AccQtyAP` | Accumulated A/P Quantity | Num | 19.6 | - |  |  |
| 8 | `AccQtyAR` | Accumulated A/R Quantity | Num | 19.6 | - |  |  |
| 9 | `AccRelQty` | Accumulated Relocated Quantity | Num | 19.6 | - |  |  |
| 10 | `CstGrpCode` | Customs Group | Int | 6 | [OARG](OARG.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
