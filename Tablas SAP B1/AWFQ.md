# AWFQ - SWFQ History Table

- **Tabla:** AWFQ
- **Descripción:** SWFQ History Table
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AWFQ.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SequenceID` | Sequence ID | Int | 11 | - |  |  |
| 2 | `SourceDB` | Source Database | nVarChar | 100 | - |  |  |
| 3 | `Timestamp` | Time Stamp | nVarChar | 20 | - |  |  |
| 4 | `ObjectType` | Object Type | nVarChar | 30 | - |  |  |
| 5 | `TransType` | Transaction Type | VarChar | 1 | - |  | `A` = Add<br>`U` = Update<br>`C` = Cancel<br>`D` = Delete |
| 6 | `FieldsInKe` | Number of Fields in Key | Int | 11 | - |  |  |
| 7 | `FieldNames` | Key Field Names | nVarChar | 254 | - |  |  |
| 8 | `FieldValue` | Key Field Values | nVarChar | 254 | - |  |  |
| 9 | `UserID` | UserID | nVarChar | 25 | - |  |  |
| 10 | `TaskID` | Task ID | nVarChar | 64 | - |  |  |
| 11 | `TrigEvntID` | Trigger Event ID | nVarChar | 64 | - |  |  |
| 12 | `TrigParams` | Trigger Parameters | Text | 16 | - |  |  |
| 13 | `LogInst` | Log Instance | Int | 11 | - |  |  |
| 14 | `IsSuccess` | Is Message Handled Successfully | VarChar | 1 | - |  |  |
| 15 | `ResultMemo` | Memo of the Result | nVarChar | 250 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SequenceID, LogInst |
