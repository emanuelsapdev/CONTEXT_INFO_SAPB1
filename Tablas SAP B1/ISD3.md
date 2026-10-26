# ISD3 - DI Input Auto Rule

- **Tabla:** ISD3
- **Descripción:** DI Input Auto Rule
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ISD3.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal ID | Int | 11 | - |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `LocCode` | Location Code | Int | 11 | - |  |  |
| 4 | `TaxAcc` | Tax Account | nVarChar | 15 | - |  |  |
| 5 | `AllocPerc` | Allocation Percentage | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
