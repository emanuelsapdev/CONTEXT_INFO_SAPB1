# AWL1 - Potential Processor of Tasks - History

- **Tabla:** AWL1
- **Descripción:** Potential Processor of Tasks - History
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AWL1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WFInstID` | Workflow Instance ID | Int | 11 | - |  |  |
| 2 | `TaskID` | Task ID | Int | 11 | [OWLS](OWLS.md) |  |  |
| 3 | `LineID` | Line ID | Int | 6 | - |  |  |
| 4 | `Candidate` | Candidate | nVarChar | 254 | - |  |  |
| 5 | `LogIns` | Log Instance | Int | 11 | - |  |  |
| 6 | `WasRead` | Was Read | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `CandExpr` | Candidate Expression | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TaskID, LineID, LogIns |
