# BPL1 - Branch I.E. Numbers

- **Tabla:** BPL1
- **Descripción:** Branch I.E. Numbers
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BPL1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BPLId` | BPL ID | Int | 11 | [OBPL](OBPL.md) |  |  |
| 2 | `DstState` | Destination State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 3 | `IENumber` | I.E. Number | nVarChar | 32 | - |  |  |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BPLId, DstState |
