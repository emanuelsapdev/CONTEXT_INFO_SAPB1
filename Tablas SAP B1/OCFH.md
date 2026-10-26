# OCFH - Cash Flow Statement History

- **Tabla:** OCFH
- **Descripción:** Cash Flow Statement History
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCFH.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CFHId` | Cash Flow History Identity | Int | 11 | - |  |  |
| 2 | `CFHName` | Saved Cash Flow Name | nVarChar | 100 | - |  |  |
| 3 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 4 | `UserName` | User Name | nVarChar | 30 | - |  |  |
| 5 | `CreateDate` | Recording Date | Date | 8 | - |  |  |
| 6 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 7 | `EndDate` | End Date | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CFHId |
