# IMPLG - Private Message Log

- **Tabla:** IMPLG
- **Descripción:** Private Message Log
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IMPLG.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | Internal Number | Identity | 11 | - |  |  |
| 2 | `Owner` | Message Owner | nVarChar | 25 | - |  |  |
| 3 | `From` | Message Sender | nVarChar | 25 | - |  |  |
| 4 | `To` | Message Receiver | nVarChar | 25 | - |  |  |
| 5 | `Msg` | Message Content | Text | 16 | - |  |  |
| 6 | `Time` | Time | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
