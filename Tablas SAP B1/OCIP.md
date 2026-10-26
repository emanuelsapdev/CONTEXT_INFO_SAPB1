# OCIP - Configuration of Integration Packages

- **Tabla:** OCIP
- **Descripción:** Configuration of Integration Packages
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCIP.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Package Code | nVarChar | 10 | - |  |  |
| 3 | `Name` | Package Name | nVarChar | 254 | - |  |  |
| 4 | `DsplID` | Display Description ID | Int | 11 | - |  |  |
| 5 | `IsEnable` | Is Enabled | VarChar | 1 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE | Yes | Code |
