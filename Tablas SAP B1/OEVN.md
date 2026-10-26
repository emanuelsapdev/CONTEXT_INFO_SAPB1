# OEVN - Event Notification

- **Tabla:** OEVN
- **Descripción:** Event Notification
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OEVN.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `EventID` | Event ID | nVarChar | 50 | - |  |  |
| 2 | `SourceDB` | Event Source Database | nVarChar | 100 | - |  |  |
| 3 | `Status` | Event Status | VarChar | 1 | - | N | `N` = New<br>`F` = Failed<br>`P` = Partially Delivered<br>`D` = Delivered<br>`A` = Archived |
| 4 | `ObjectType` | Object Type | nVarChar | 30 | - |  |  |
| 5 | `BizObject` | Business Object | nVarChar | 64 | - |  |  |
| 6 | `TransType` | Transaction Type | VarChar | 1 | - |  |  |
| 7 | `Operation` | Transaction Operation | nVarChar | 64 | - |  |  |
| 8 | `FieldsInKe` | Number of Key Fields | Int | 11 | - |  |  |
| 9 | `FieldNames` | Names of Key Fields | nVarChar | 254 | - |  |  |
| 10 | `FieldValue` | Values of Key Fields | nVarChar | 254 | - |  |  |
| 11 | `ReplayStat` | Replay State | VarChar | 1 | - | N | `N` = None<br>`R` = Replaying<br>`C` = Completed |
| 12 | `UserID` | User ID | nVarChar | 25 | - |  |  |
| 13 | `SAPPassprt` | Extended SAP Passport | Text | 16 | - |  |  |
| 14 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 15 | `CreateTime` | Creation Timestamp | Int | 11 | - |  |  |
| 16 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 17 | `UpdateTime` | Update Timestamp | Int | 11 | - |  |  |
| 18 | `KeyData` | Key Properties/Values | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | EventID |
