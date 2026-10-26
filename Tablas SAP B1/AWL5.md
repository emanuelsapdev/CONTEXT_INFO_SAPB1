# AWL5 - Task Field Mapping Information - History

- **Tabla:** AWL5
- **Descripción:** Task Field Mapping Information - History
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AWL5.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WFInstID` | Workflow Instance ID | nVarChar | 64 | - |  |  |
| 2 | `TaskID` | Task ID | Int | 11 | [OWLS](OWLS.md) |  |  |
| 3 | `LineID` | Line ID | nVarChar | 6 | - |  |  |
| 4 | `InputID` | Input ID | Int | 11 | - |  |  |
| 5 | `SrcFld` | Source Field | nVarChar | 50 | - |  |  |
| 6 | `TgtFld` | Target Field | nVarChar | 50 | - |  |  |
| 7 | `LogIns` | Log Instance | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TaskID, LineID, LogIns |
