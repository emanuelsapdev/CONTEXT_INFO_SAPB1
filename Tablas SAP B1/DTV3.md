# DTV3 - Datev Run Lines Cards

- **Tabla:** DTV3
- **Descripción:** Datev Run Lines Cards
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DTV3.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RunId` | Run Number | Int | 11 | [ODTV](ODTV.md) |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `CardCode` | Customer Number | nVarChar | 50 | - |  |  |
| 4 | `CardName` | Customer Name | nVarChar | 100 | - |  |  |
| 5 | `CardType` | Customer Type | VarChar | 1 | - |  | `C` = Customer<br>`S` = Supplier |
| 6 | `Text` | Run results | Text | 16 | - |  |  |
| 7 | `Detail` | Run Details | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RunId, LineId |
