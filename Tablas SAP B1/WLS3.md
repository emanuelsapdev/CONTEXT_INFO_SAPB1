# WLS3 - Notes of Tasks

- **Tabla:** WLS3
- **Descripción:** Notes of Tasks
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WLS3.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WFInstID` | Workflow Instance ID | Int | 11 | - |  |  |
| 2 | `TaskID` | Task ID | Int | 11 | [OWLS](OWLS.md) |  |  |
| 3 | `LineID` | Line ID | Int | 11 | - |  |  |
| 4 | `Note` | Note | Text | 16 | - |  |  |
| 5 | `Creator` | Creator | nVarChar | 25 | - |  |  |
| 6 | `NoteDate` | Note Date | Date | 8 | - |  |  |
| 7 | `Access` | Accessibility | VarChar | 1 | - | W | `W` = Workflow<br>`T` = Task |
| 8 | `LogIns` | Log Instance | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TaskID, LineID |
