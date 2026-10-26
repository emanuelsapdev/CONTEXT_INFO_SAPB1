# SWFQ - SWFQ

- **Tabla:** SWFQ
- **Descripción:** SWFQ
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SWFQ.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SequenceID` | Sequence ID | Int | 11 | - |  |  |
| 2 | `SourceDB` | Source DB | nVarChar | 100 | - |  |  |
| 3 | `Timestamp` | Timestamp | nVarChar | 20 | - |  |  |
| 4 | `ObjectType` | Object Type | nVarChar | 30 | - |  |  |
| 5 | `TransType` | Transaction Type | VarChar | 1 | - |  | `A` = Add<br>`U` = Update<br>`C` = Cancel<br>`D` = Delete |
| 6 | `FieldsInKe` | Number of fields in key | Int | 11 | - |  |  |
| 7 | `FieldNames` | Key Field Names | nVarChar | 254 | - |  |  |
| 8 | `FieldValue` | Key Field Values | nVarChar | 254 | - |  |  |
| 9 | `UserID` | UserID | nVarChar | 25 | - |  |  |
| 10 | `TaskID` | TaskID | nVarChar | 64 | - |  |  |
| 11 | `TrigEvntID` | Trigger Event ID | nVarChar | 64 | - |  |  |
| 12 | `TrigParams` | Trigger parameters | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SequenceID |
