# HET1 - Employee Transfer Details

- **Tabla:** HET1
- **Descripción:** Employee Transfer Details
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/HET1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TransferID` | Foreign Key to OHET | Int | 11 | [OHET](OHET.md) |  |  |
| 2 | `empID` | Foreign Key to OHEM | Int | 11 | [OHEM](OHEM.md) |  |  |
| 3 | `Transfered` | Timestamp: Status "Sent" | Date | 8 | - |  |  |
| 4 | `Status` | Processing Status | VarChar | 1 | - | N | `N` = New<br>`S` = Sent<br>`A` = Accepted<br>`E` = Error |
| 5 | `Comment` | Any comments | Text | 16 | - |  |  |
| 6 | `TransTime` | Time When Status Is "Sent" | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TransferID, empID |
