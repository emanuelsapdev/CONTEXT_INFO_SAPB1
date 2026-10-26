# TRS2 - Tax Rpt Sav Obj Man Chgd Vals

- **Tabla:** TRS2
- **Descripción:** Tax Rpt Sav Obj Man Chgd Vals
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TRS2.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 3 | `LineID` | Internal Row Number | Int | 11 | - |  |  |
| 4 | `ParamCode` | Parameter Code | nVarChar | 32 | - |  |  |
| 5 | `PrmValAmt` | Parameter Value Amount | Num | 19.6 | - |  |  |
| 6 | `PrmValNum` | Parameter Value Number | Int | 11 | - |  |  |
| 7 | `PrmValStr` | Parameter Value String | nVarChar | 254 | - |  |  |
| 8 | `PrmValTxt` | Parameter Value Text | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineID |
| SECONDARY | Yes | AbsEntry, ParamCode |
