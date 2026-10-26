# CRD14 - Business Partners Bookkeeping Certified Dates

- **Tabla:** CRD14
- **Descripción:** Business Partners Bookkeeping Certified Dates
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CRD14.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 2 | `ValidFrom` | Valid From Date | Date | 8 | - |  |  |
| 3 | `ValidTo` | Valid To Date | Date | 8 | - |  |  |
| 4 | `UpdateDate` | Last Update Date | Date | 8 | - |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode, ValidFrom |
