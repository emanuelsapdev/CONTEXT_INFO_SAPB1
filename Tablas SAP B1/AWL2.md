# AWL2 - Input Data of Tasks - History

- **Tabla:** AWL2
- **Descripción:** Input Data of Tasks - History
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AWL2.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WFInstID` | Workflow Instance ID | Int | 11 | - |  |  |
| 2 | `TaskID` | Task ID | Int | 11 | [OWLS](OWLS.md) |  |  |
| 3 | `LineID` | Line ID | Int | 11 | - |  |  |
| 4 | `ObjectType` | Object Type | nVarChar | 20 | - |  |  |
| 5 | `ObjKey` | Object Key | nVarChar | 100 | - |  |  |
| 6 | `Command` | Command | VarChar | 1 | - | B | `B` = Based On<br>`M` = Field Mapping |
| 7 | `LogIns` | Log Instance | Int | 11 | - |  |  |
| 8 | `ObjSubType` | Object Subtype | nVarChar | 64 | - |  |  |
| 9 | `ObjDetail` | Object Detail | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TaskID, LineID, LogIns |
