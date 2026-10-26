# OWMG - Workflow Manager

- **Tabla:** OWMG
- **Descripción:** Workflow Manager
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWMG.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ID` | Workflow ID | Identity | 11 | - |  |  |
| 2 | `TemplateID` | Template ID | Int | 11 | - |  |  |
| 3 | `TmplateKey` | Template Key | nVarChar | 254 | - |  |  |
| 4 | `Name` | Name | nVarChar | 254 | - |  |  |
| 5 | `Version` | Version | nVarChar | 13 | - |  |  |
| 6 | `MAXIns` | Maximum Number of Instances | Int | 11 | - |  |  |
| 7 | `Status` | Status | VarChar | 1 | - | I | `I` = Inactive<br>`A` = Active<br>`E` = Activation failed<br>`M` = Importing<br>`P` = Imported<br>`F` = Import failed<br>`D` = Deleted |
| 8 | `XMLFile` | XML File | Text | 16 | - |  |  |
| 9 | `Desc` | Description | Text | 16 | - |  |  |
| 10 | `LogIns` | Log Instance - History | Int | 11 | - |  |  |
| 11 | `StartType` | Start Type | VarChar | 1 | - | M | `M` = Manual Start<br>`T` = Timer Start<br>`C` = Conditional Start |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
