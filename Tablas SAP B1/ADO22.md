# ADO22 - Marketing Document (Resource Costs) - History

- **Tabla:** ADO22
- **Descripción:** Marketing Document (Resource Costs) - History
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ADO22.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [ADO1](ADO1.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | [ADO1](ADO1.md) |  |  |
| 3 | `StdCostNum` | Resource Standard Cost Number | Int | 11 | - |  |  |
| 4 | `Price` | Price | Num | 19.6 | - |  |  |
| 5 | `Total` | Total | Num | 19.6 | - |  |  |
| 6 | `ObjectType` | Object Type | nVarChar | 20 | - | 13 |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, StdCostNum, LogInstanc, ObjectType |
