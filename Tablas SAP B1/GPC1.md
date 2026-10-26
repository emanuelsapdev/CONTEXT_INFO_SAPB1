# GPC1 - Authority Assignment

- **Tabla:** GPC1
- **Descripción:** Authority Assignment
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GPC1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | [OGPC](OGPC.md) |  |  |
| 2 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 3 | `State` | State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 4 | `CardCode` | Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId, BPLId, State |
| CARD_CODE | Yes | CardCode |
