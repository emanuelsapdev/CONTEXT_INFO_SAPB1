# HLD1 - Holiday Dates

- **Tabla:** HLD1
- **Descripción:** Holiday Dates
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/HLD1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `HldCode` | Holiday Code | nVarChar | 20 | [OHLD](OHLD.md) |  |  |
| 2 | `StrDate` | Start Date | Date | 8 | - |  |  |
| 3 | `EndDate` | End Date | Date | 8 | - |  |  |
| 4 | `Rmrks` | Remarks | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | HldCode, StrDate, EndDate |
