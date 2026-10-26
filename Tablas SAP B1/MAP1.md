# MAP1 - Input and Output of Mapping

- **Tabla:** MAP1
- **Descripción:** Input and Output of Mapping
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MAP1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MapID` | Mapping ID | Int | 11 | [OMAP](OMAP.md) |  |  |
| 2 | `Code` | Code | Int | 11 | - |  |  |
| 3 | `Type` | Type | nVarChar | 10 | - | NA | `CRYSTAL` = Crystal Report<br>`XML` = XML File<br>`NA` = Not Avalible<br>`TXT` = Text File<br>`CSV` = CSV File |
| 4 | `RuleType` | Rule Type | nVarChar | 10 | - | NA | `XSLT` = XSLT Rule<br>`NA` = Not Avalible<br>`REGEX` = Reguler expression |
| 5 | `RuleRef` | Rule Reference ID | nVarChar | 50 | - |  |  |
| 6 | `RefID` | Reference ID | nVarChar | 50 | - |  |  |
| 7 | `RuleVer` | Rule Version | nVarChar | 5 | - |  |  |
| 8 | `IsFinal` | Is Final Result | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MapID, Code |
