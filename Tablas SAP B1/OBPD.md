# OBPD - Blocked Personal Data

- **Tabla:** OBPD
- **Descripción:** Blocked Personal Data
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBPD.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DatSubType` | Data Subject Type | nVarChar | 4 | - |  | `OCRD` = Business Partner<br>`OCPR` = Contact Person<br>`OHEM` = Employee<br>`OUSR` = User<br>`CPN1` = Campaign - BP<br>`OUDO` = User-Defined Object |
| 3 | `DatSubKey` | Data Subject Key No.1 | nVarChar | 15 | - |  |  |
| 4 | `DatSubKey2` | Data Subject Key No.2 | nVarChar | 50 | - |  |  |
| 5 | `TableName` | Table Name | nVarChar | 21 | - |  |  |
| 6 | `KeyValue1` | Key Value No.1 | nVarChar | 50 | - |  |  |
| 7 | `KeyValue2` | Key Value No.2 | nVarChar | 50 | - |  |  |
| 8 | `KeyValue3` | Key Value No.3 | nVarChar | 50 | - |  |  |
| 9 | `KeyValue4` | Key Value No.4 | nVarChar | 50 | - |  |  |
| 10 | `KeyValue5` | Key Value No.5 | nVarChar | 50 | - |  |  |
| 11 | `FieldName` | Field Name | nVarChar | 52 | - |  |  |
| 12 | `EncryptVal` | Encryption Value | Text | 16 | - |  |  |
| 13 | `EncryptIV` | Encryption Initialization Vector | nVarChar | 100 | - |  |  |
| 14 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 15 | `CreateTime` | Creation Time | Int | 11 | - |  |  |
| 16 | `ObjType` | Object Type | nVarChar | 20 | - | -1 |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| DATA_SUBJ | No | DatSubType, DatSubKey, DatSubKey2 |
| TABL_FIELD | No | TableName, KeyValue1, KeyValue2, KeyValue3, KeyValue4, KeyValue5, FieldName |
