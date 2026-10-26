# OPTF - BoE Portfolio

- **Tabla:** OPTF
- **Descripción:** BoE Portfolio
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPTF.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `PtfId` | Internal Portfolio ID | nVarChar | 3 | - |  |  |
| 3 | `PtfCode` | Portfolio Code | nVarChar | 2 | - |  |  |
| 4 | `PtfNum` | Portfolio Number | nVarChar | 4 | - |  |  |
| 5 | `PtfDespt` | Description | nVarChar | 20 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| ID | Yes | PtfId |
