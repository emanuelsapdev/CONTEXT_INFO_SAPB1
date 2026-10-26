# REQ2 - External System Call Request - Argument List

- **Tabla:** REQ2
- **Descripción:** External System Call Request - Argument List
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/REQ2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Request ID | Int | 11 | [OREQ](OREQ.md) |  |  |
| 2 | `LineId` | Message Line ID | Int | 11 | - | 1 |  |
| 3 | `ArgName` | Argument Name | nVarChar | 20 | - |  |  |
| 4 | `ArgValue` | Argument Value | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId, ArgName |
