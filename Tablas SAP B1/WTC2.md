# WTC2 - WTax Certificates - Docs in WT Groups

- **Tabla:** WTC2
- **Descripción:** WTax Certificates - Docs in WT Groups
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WTC2.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `BaseLineId` | Base Line Number | Int | 11 | - |  |  |
| 3 | `LineId` | Line Number | Int | 11 | - |  |  |
| 4 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 5 | `DocObjType` | Doc. Object Type | nVarChar | 20 | - |  |  |
| 6 | `VatAmnt` | VAT Amount | Num | 19.6 | - |  |  |
| 7 | `DocTot` | Doc. Total Amount | Num | 19.6 | - |  |  |
| 8 | `WTBaseAmnt` | WTax Base Amount | Num | 19.6 | - |  |  |
| 9 | `WTAccAmnt` | Accumulated Amount | Num | 19.6 | - |  |  |
| 10 | `WTPercpAm` | WTax Perception Amount | Num | 19.6 | - |  |  |
| 11 | `WTPercent` | WTax Rate | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, BaseLineId, LineId |
