# OLGL - Legal Data

- **Tabla:** OLGL
- **Descripción:** Legal Data
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OLGL.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `SrcObjType` | Source Object Type | nVarChar | 20 | - | -1 | `-1`<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo |
| 3 | `SrcObjAbs` | Source Object Internal ID | Int | 11 | - | -1 |  |
| 4 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 540000073 |  |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `PrintDate` | Date of Printing | Date | 8 | - |  |  |
| 7 | `PrintTime` | Time of Printing | Int | 6 | - |  |  |
| 8 | `PrBrand` | Printer Brand | nVarChar | 30 | - |  |  |
| 9 | `PrType` | Printer Type | nVarChar | 30 | - |  |  |
| 10 | `PrModel` | Printer Model | nVarChar | 30 | - |  |  |
| 11 | `PrFwVer` | Printer Firmware Version | nVarChar | 30 | - |  |  |
| 12 | `PrDllVer` | Printer DLL Version | nVarChar | 30 | - |  |  |
| 13 | `FisSeries` | Fiscal Series | nVarChar | 30 | - |  |  |
| 14 | `FisNumber` | Fiscal Number | nVarChar | 30 | - |  |  |
| 15 | `DocNumber` | Document Number | nVarChar | 30 | - |  |  |
| 16 | `FisUser` | Fiscal User ID | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SRC_DOC | Yes | SrcObjType, SrcObjAbs |
