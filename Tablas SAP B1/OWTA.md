# OWTA - Withholding Tax Accumulation

- **Tabla:** OWTA
- **Descripción:** Withholding Tax Accumulation
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWTA.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `PmntDate` | Payment Date | Date | 8 | - |  |  |
| 4 | `WTTypeId` | WT Type Id | Int | 11 | - |  |  |
| 5 | `AccmAmnt` | WT Accumulated Amount | Num | 19.6 | - |  |  |
| 6 | `AccmAmntFC` | WT Accumulated Amount FC | Num | 19.6 | - |  |  |
| 7 | `AccmAmntSC` | WT Accumulated Amount SC | Num | 19.6 | - |  |  |
| 8 | `BPLId` | Branch | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SECONDARY | Yes | CardCode, PmntDate, WTTypeId, BPLId |
