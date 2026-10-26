# TXD2 - Tax Invoice Draft Operation Codes

- **Tabla:** TXD2
- **Descripción:** Tax Invoice Draft Operation Codes
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TXD2.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BaseEntry` | Abs. Entry | Int | 11 | [OTSI](OTSI.md) |  |  |
| 2 | `LineNum` | Base Doc. Abs. Entry | Int | 11 | [TSI1](TSI1.md) |  |  |
| 3 | `OpCode` | Operation Code | Int | 11 | [OBSI](OBSI.md) |  |  |
| 4 | `ObjType` | Object Type | Int | 11 | [ADP1](ADP1.md) |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BaseEntry, LineNum, OpCode |
