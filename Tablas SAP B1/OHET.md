# OHET - Object: HR Employee Transfer

- **Tabla:** OHET
- **Descripción:** Object: HR Employee Transfer
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OHET.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TransferID` | Unique ID for Transfer | Int | 11 | - |  |  |
| 2 | `TransStart` | Transfer Start Date | Date | 8 | - |  |  |
| 3 | `TransEnd` | Timestamp if Status is "Sent" | Date | 8 | - |  |  |
| 4 | `Status` | Processing Status | VarChar | 1 | - | N | `N` = New<br>`P` = Processing<br>`S` = Sent<br>`R` = Received<br>`A` = Accepted<br>`E` = Error |
| 5 | `Comment` | Any comments | Text | 16 | - |  |  |
| 6 | `StartTime` | Transfer Start Time | Int | 6 | - |  |  |
| 7 | `EndTime` | Time When Status Is "Sent" | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TransferID |
