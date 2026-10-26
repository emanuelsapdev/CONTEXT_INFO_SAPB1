# UXILM - IVI Irrelevant Message IDs

- **Tabla:** UXILM
- **Descripción:** IVI Irrelevant Message IDs
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UXILM.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MessageID` | Message ID | Int | 11 | - |  |  |
| 2 | `MinMsgID` | MINMessage ID | Int | 11 | - |  |  |
| 3 | `MaxMsgID` | MaxMessage ID | Int | 11 | - |  |  |
| 4 | `DocEntry` | Doc Number | Int | 11 | - |  |  |
| 5 | `DocLineNum` | Doc Row Number | Int | 11 | - |  |  |
| 6 | `TransType` | Transaction Type | Int | 11 | - | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MessageID |
