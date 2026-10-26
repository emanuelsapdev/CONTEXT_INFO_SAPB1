# SEVT - SEVT

- **Tabla:** SEVT
- **Descripción:** SEVT
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SEVT.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SequenceID` | Sequence ID | Identity | 11 | - |  |  |
| 2 | `SourceDB` | Event source database | nVarChar | 100 | - |  |  |
| 3 | `Timestamp` | Event timestamp | nVarChar | 20 | - |  |  |
| 4 | `Status` | Event status | nVarChar | 50 | - |  |  |
| 5 | `Retry` | Sending event retries | Int | 11 | - |  |  |
| 6 | `ObjectType` | Object type | nVarChar | 30 | - |  |  |
| 7 | `TransType` | Transaction type | VarChar | 1 | - |  |  |
| 8 | `FieldsInKe` | Number of fields in key | Int | 11 | - |  |  |
| 9 | `FieldNames` | Names of key fields | nVarChar | 254 | - |  |  |
| 10 | `FieldValue` | Values of key fields | nVarChar | 254 | - |  |  |
| 11 | `UserID` | Modified by user | nVarChar | 155 | - |  |  |
| 12 | `USER_CODE` | User code | nVarChar | 25 | - |  |  |
| 13 | `SAPPassprt` | Extended SAP Passport | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SequenceID |
| SOURCE_DB | No | SourceDB, ObjectType, FieldValue |
