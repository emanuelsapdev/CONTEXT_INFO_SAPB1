# ITM6 - Asset Item Distribution Rules

- **Tabla:** ITM6
- **Descripción:** Asset Item Distribution Rules
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITM6.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `ValidFrom` | Valid From | Date | 8 | - |  |  |
| 4 | `ValidTo` | Valid To | Date | 8 | - |  |  |
| 5 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 6 | `OcrCode2` | Costing Code 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 7 | `OcrCode3` | Costing Code 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 8 | `OcrCode4` | Costing Code 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 9 | `OcrCode5` | Costing Code 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 10 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 11 | `ObjType` | Object | nVarChar | 20 | [ADP1](ADP1.md) | 4 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode, LineNum |
