# OPRO - Property Object

- **Tabla:** OPRO
- **Descripción:** Property Object
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPRO.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Property ID | Int | 11 | - |  |  |
| 2 | `MapID` | Mapping ID | Int | 11 | [OMAP](OMAP.md) |  |  |
| 3 | `Code` | Input/Output Code | Int | 11 | - |  |  |
| 4 | `Type` | Property Type | nVarChar | 6 | - | Strin | `Strin` = String<br>`XML` = XML<br>`String` |
| 5 | `Name` | Property Name | nVarChar | 50 | - |  |  |
| 6 | `IsBlob` | Is BLOB Type | VarChar | 1 | - |  | `Y`<br>`N` |
| 7 | `TValue` | Text Value | nVarChar | 250 | - |  |  |
| 8 | `BValue` | BLOB Value | Text | 16 | - |  |  |
| 9 | `Encoding` | Encoding | nVarChar | 20 | - |  | `base64` |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE_NAME | Yes | MapID, Code, Name |
