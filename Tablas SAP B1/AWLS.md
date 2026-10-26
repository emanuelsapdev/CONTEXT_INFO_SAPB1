# AWLS - Workflow - Task Details - History

- **Tabla:** AWLS
- **Descripción:** Workflow - Task Details - History
- **Cantidad de campos:** 34
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AWLS.html

## Campos (34)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WFInstID` | Workflow Instance ID | Int | 11 | [OWFI](OWFI.md) |  |  |
| 2 | `TaskID` | Task ID | Int | 11 | - |  |  |
| 3 | `WFID` | Workflow ID | nVarChar | 64 | - |  |  |
| 4 | `WFName` | Workflow Name | nVarChar | 100 | - |  |  |
| 5 | `TaskDesc` | Task Description | nVarChar | 100 | - |  |  |
| 6 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 7 | `Operation` | Operation | VarChar | 1 | - |  | `A` = Add<br>`U` = Update<br>`D` = Delete |
| 8 | `ObjKey` | Object Key | nVarChar | 100 | - |  |  |
| 9 | `EnterDate` | Enter Date | Date | 8 | - |  |  |
| 10 | `EnterTime` | Enter Time | Int | 6 | - |  |  |
| 11 | `TaskType` | Task Type | VarChar | 1 | - |  |  |
| 12 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 13 | `DueTime` | Due Time | Int | 6 | - |  |  |
| 14 | `UpdateDate` | Update Date - History | Date | 8 | - |  |  |
| 15 | `UpdateTime` | Update Time - History | Int | 6 | - |  |  |
| 16 | `Owner` | Owner | nVarChar | 25 | - |  |  |
| 17 | `Priority` | Priority | Int | 6 | - | 2 | `1` = High<br>`2` = Medium<br>`3` = Low |
| 18 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 19 | `Status` | Status | VarChar | 1 | - | W | `S` = Setup<br>`W` = To Be Picked<br>`P` = Picking<br>`G` = In Progress<br>`D` = Completing<br>`F` = Completed<br>`N` = Suspended<br>`C` = Cancelling<br>`Q` = Canceled<br>`O` = Forwarding<br>`E` = Error |
| 20 | `LogIns` | Log Instance - History | Int | 11 | - |  |  |
| 21 | `UserSign2` | Updating User - History | Int | 6 | - |  |  |
| 22 | `Deleted` | Deleted - History | VarChar | 1 | - |  |  |
| 23 | `DuraDays` | Duration Days | Int | 11 | - |  |  |
| 24 | `DuraHours` | Duration Hours | Int | 6 | - |  |  |
| 25 | `TaskName` | Task Name | nVarChar | 100 | - |  |  |
| 26 | `isPicked` | Is Picked | VarChar | 1 | - | N |  |
| 27 | `Attachment` | Attachment | Text | 16 | - |  |  |
| 28 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 29 | `WorkListId` | Worklist ID | Int | 11 | - |  |  |
| 30 | `ObjSubType` | Object Subtype | nVarChar | 64 | - |  |  |
| 31 | `ForwardTo` | User to Forward | nVarChar | 25 | - |  |  |
| 32 | `WasRead` | Line Read | VarChar | 1 | - | N |  |
| 33 | `TrigParams` | Trigger Parameters | Text | 16 | - |  |  |
| 34 | `Key` | Task ID in XML | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TaskID, LogIns |
