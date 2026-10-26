# USR6 - User Branch Assignment

- **Tabla:** USR6
- **Descripción:** User Branch Assignment
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/USR6.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UserCode` | User Code | nVarChar | 25 | [OUSR](OUSR.md) |  |  |
| 2 | `BPLId` | Assigned Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 3 | `DigCrtPath` | Digital Certificate Path | Text | 16 | - |  |  |
| 4 | `AcsDsbldBP` | Access Disabled BP | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `UserID` | User ID | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UserCode, BPLId |
