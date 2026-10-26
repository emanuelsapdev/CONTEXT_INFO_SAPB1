# GDP1 - General Data Protection Wizard - Personal Fields Setup

- **Tabla:** GDP1
- **Descripción:** General Data Protection Wizard - Personal Fields Setup
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GDP1.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `PfsAbs` | Internal Number | Int | 11 | - |  |  |
| 3 | `TableName` | Table Name | nVarChar | 20 | - |  |  |
| 4 | `FieldName` | Field Name | nVarChar | 50 | - |  |  |
| 5 | `RefObjType` | Referenced Object Type | nVarChar | 20 | - |  |  |
| 6 | `Category` | Category | VarChar | 1 | - | N | `N`<br>`R` = Sales A/R<br>`P` = Purchase A/P |
| 7 | `OrigType` | Original Type | VarChar | 1 | - | U | `U` = User Defined<br>`S` = Sensitive<br>`P` = Personal<br>`N` = Not Personal |
| 8 | `Type` | Type | VarChar | 1 | - | N | `N` = Not Relevant<br>`S` = Sensitive<br>`P` = Personal |
| 9 | `Descr` | Description | nVarChar | 254 | - |  |  |
| 10 | `MaxType` | Max. Type | VarChar | 1 | - | U | `U` = User Defined<br>`S` = Sensitive<br>`P` = Personal |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, PfsAbs |
