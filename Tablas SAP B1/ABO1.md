# ABO1 - External Bank Operation Code - Rows - Log

- **Tabla:** ABO1
- **Descripción:** External Bank Operation Code - Rows - Log
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ABO1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OBOC](OBOC.md) |  |  |
| 2 | `ExOpCode` | External Bank Operation Code | nVarChar | 40 | - |  |  |
| 3 | `OPDscrpt` | Operation Description | nVarChar | 40 | - |  |  |
| 4 | `InOpCode` | Internal Bank Operation Code | Int | 11 | [OBTC](OBTC.md) |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 6 | `LineId` | Row | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId, LogInstanc |
