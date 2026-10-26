# WLS4 - Task Output Data

- **Tabla:** WLS4
- **Descripción:** Task Output Data
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WLS4.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WFInstID` | Workflow Instance ID | nVarChar | 64 | - |  |  |
| 2 | `TaskID` | Task ID | Int | 11 | [OWLS](OWLS.md) |  |  |
| 3 | `LineID` | Line ID | nVarChar | 6 | - |  |  |
| 4 | `ObjectType` | Object Type | nVarChar | 20 | - |  |  |
| 5 | `ObjKey` | Object Key | nVarChar | 100 | - |  |  |
| 6 | `LogIns` | Log Instance | Int | 11 | - |  |  |
| 7 | `OutParamID` | Object ID in WF Engine | nVarChar | 64 | - |  |  |
| 8 | `ObjSubType` | Object Subtype | nVarChar | 64 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TaskID, LineID |
