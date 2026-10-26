# ZRD1 - POS Daily Summary - Totals

- **Tabla:** ZRD1
- **Descripción:** POS Daily Summary - Totals
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ZRD1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Document Internal ID | Int | 11 | [OZRD](OZRD.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `Code` | Totalizer Code | nVarChar | 8 | - |  |  |
| 4 | `Number` | Totalizer Number | Int | 11 | - |  |  |
| 5 | `TotalSum` | Total Sum | Num | 19.6 | - |  |  |
| 6 | `Descriptn` | Description | nVarChar | 254 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
| CODE | Yes | Code, AbsEntry |
