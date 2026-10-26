# OQUE - Queue

- **Tabla:** OQUE
- **Descripción:** Queue
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OQUE.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `queueID` | Queue ID | nVarChar | 20 | - |  |  |
| 2 | `descript` | Description | nVarChar | 200 | - |  |  |
| 3 | `manager` | Queue Manager | Int | 11 | [OUSR](OUSR.md) | 0 |  |
| 4 | `email` | Queue E-Mail | nVarChar | 200 | - |  |  |
| 5 | `inactive` | Inactive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | queueID |
