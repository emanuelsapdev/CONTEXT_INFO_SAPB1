# SVM1 - Systems for Value Mapping Properties

- **Tabla:** SVM1
- **Descripción:** Systems for Value Mapping Properties
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SVM1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `PropID` | Property ID | Int | 11 | - |  |  |
| 3 | `PropDesc` | Property Description | nVarChar | 50 | - |  |  |
| 4 | `PropType` | Property Type | VarChar | 1 | - | S | `S` = String<br>`N` = Numeric<br>`D` = Date<br>`P` = Password |
| 5 | `PropValue` | Property Value | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, PropID |
