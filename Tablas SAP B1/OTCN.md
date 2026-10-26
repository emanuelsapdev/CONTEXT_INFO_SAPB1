# OTCN - Tracking Note

- **Tabla:** OTCN
- **Descripción:** Tracking Note
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTCN.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Abs. Entry | Int | 11 | - |  |  |
| 2 | `CCDNum` | CCD Number | nVarChar | 40 | - |  |  |
| 3 | `Date` | Date | Date | 8 | - |  |  |
| 4 | `CustTerm` | Customs Terminal | nVarChar | 15 | - |  |  |
| 5 | `CntrOrigin` | Country/Region of Origin | nVarChar | 3 | - |  |  |
| 6 | `DirectImp` | Direct Import | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `CardCode` | BP Code | nVarChar | 15 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CCD | Yes | CCDNum, DirectImp |
