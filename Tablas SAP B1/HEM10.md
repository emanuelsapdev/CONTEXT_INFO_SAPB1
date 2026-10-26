# HEM10 - Employee Branch Assignment

- **Tabla:** HEM10
- **Descripción:** Employee Branch Assignment
- **Cantidad de campos:** 2
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/HEM10.html

## Campos (2)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `empID` | Employee No. | Int | 11 | - |  |  |
| 2 | `BPLId` | Assigned Branch | Int | 11 | [OBPL](OBPL.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | empID, BPLId |
