# HMM1 - Child Table of OHMM

- **Tabla:** HMM1
- **Descripción:** Child Table of OHMM
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/HMM1.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | [OHMM](OHMM.md) |  |  |
| 2 | `LineNum` | Child No. | Int | 11 | - |  |  |
| 3 | `ViewType` | View Type | VarChar | 1 | - |  | `A` = Attribute View<br>`C` = Calculation View<br>`Y` = Analytic View<br>`P` = Procedure |
| 4 | `ViewName` | View Name | nVarChar | 100 | - |  |  |
| 5 | `MenuDesc` | Menu Description | nVarChar | 254 | - |  |  |
| 6 | `MenuEnable` | Menu Enable | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 7 | `IAEnable` | Interactive Analysis Enable | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `SLEnable` | Enable Service Layer | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 9 | `SLExpose` | Expose Service Layer | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
| UNIQUEVIEW | Yes | ViewName |
