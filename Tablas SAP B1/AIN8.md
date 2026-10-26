# AIN8 - Inventory Counting - Individual Counters - History

- **Tabla:** AIN8
- **Descripción:** Inventory Counting - Individual Counters - History
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AIN8.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | [OINC](OINC.md) |  |  |
| 2 | `CounterNum` | Counter Number | Int | 11 | - |  |  |
| 3 | `CounteType` | Type of Counter | Int | 11 | - | 12 | `12` = User<br>`171` = Employee |
| 4 | `CounterId` | Counter ID | Int | 11 | - |  |  |
| 5 | `CounteName` | Counter Name | nVarChar | 155 | - |  |  |
| 6 | `LogIns` | Log Instance - History | Int | 11 | - |  |  |
| 7 | `VisOrder` | Visual Order | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, CounterNum, LogIns |
| BUSINESS | Yes | DocEntry, CounteType, CounterId, LogIns |
