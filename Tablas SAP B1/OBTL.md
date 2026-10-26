# OBTL - Bin Transaction Log

- **Tabla:** OBTL
- **Descripción:** Bin Transaction Log
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBTL.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `MessageID` | ILM Message ID | Int | 11 | [OILM](OILM.md) |  |  |
| 3 | `BinAbs` | Bin Internal Number | Int | 11 | [OBIN](OBIN.md) |  |  |
| 4 | `SnBMDAbs` | SnB Master Data Internal Number | Int | 11 | - | -1 |  |
| 5 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 6 | `ITLEntry` | ITL Log Internal ID | Int | 11 | [OITL](OITL.md) | -1 |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| MESSAGE_ID | No | MessageID |
| BIN_ABS | No | BinAbs |
