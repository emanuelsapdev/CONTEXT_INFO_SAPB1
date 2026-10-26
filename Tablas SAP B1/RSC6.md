# RSC6 - Resources - Daily Capacities

- **Tabla:** RSC6
- **Descripción:** Resources - Daily Capacities
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RSC6.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ResCode` | Internal Resource ID | nVarChar | 50 | [ORSC](ORSC.md) |  |  |
| 2 | `WeekDay` | Weekday No. | Int | 11 | - | 1 | `1` = First Day of Week<br>`2` = Second Day of Week<br>`3` = Third Day of Week<br>`4` = Fourth Day of Week<br>`5` = Fifth Day of Week<br>`6` = Sixth Day of Week<br>`7` = Seventh Day of Week |
| 3 | `CapFactor1` | Day 1 Capacity Factor 1 | Num | 19.6 | - |  |  |
| 4 | `CapFactor2` | Day 1 Capacity Factor 2 | Num | 19.6 | - |  |  |
| 5 | `CapFactor3` | Day 1 Capacity Factor 3 | Num | 19.6 | - |  |  |
| 6 | `CapFactor4` | Day 1 Capacity Factor 4 | Num | 19.6 | - |  |  |
| 7 | `CapTotal` | Total Daily Capacity | Num | 19.6 | - |  |  |
| 8 | `Remarks` | Remarks | nVarChar | 100 | - |  |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 10 | `SngRunCap` | Single Run Capacity | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ResCode, WeekDay |
