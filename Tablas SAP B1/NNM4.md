# NNM4 - Electronic Series

- **Tabla:** NNM4
- **Descripción:** Electronic Series
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/NNM4.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ESeries` | Electronic Series | Int | 6 | - | 0 |  |
| 2 | `Series` | Series | Int | 11 | - |  |  |
| 3 | `SeriesName` | Series Name | nVarChar | 8 | - |  |  |
| 4 | `InitialNum` | Initial Number | nVarChar | 20 | - | 0 |  |
| 5 | `NextNumber` | Next Number for Use | nVarChar | 20 | - | 0 |  |
| 6 | `LastNum` | Last Number Allowed | nVarChar | 20 | - |  |  |
| 7 | `Prefix` | Prefix | nVarChar | 10 | - |  |  |
| 8 | `ApprovYear` | Approval Year | Int | 11 | - |  |  |
| 9 | `ApprovNum` | Approval Number | Int | 11 | - |  |  |
| 10 | `Remark` | Remarks | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ESeries, InitialNum |
