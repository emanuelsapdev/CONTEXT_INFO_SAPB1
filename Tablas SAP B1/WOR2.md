# WOR2 - Production Order - Base

- **Tabla:** WOR2
- **Descripción:** Production Order - Base
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WOR2.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal Number | Int | 11 | [OWOR](OWOR.md) |  |  |
| 2 | `BaseEntry` | Production Order Base Entry | Int | 11 | [ORDR](ORDR.md) |  |  |
| 3 | `BaseNum` | Production Order Base Number | Int | 11 | - |  |  |
| 4 | `BaseLine` | Production Order Base Line | Int | 11 | - |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, BaseEntry, BaseLine |
