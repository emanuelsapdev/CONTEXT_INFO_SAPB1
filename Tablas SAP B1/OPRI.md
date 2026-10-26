# OPRI - Browser Access Printers

- **Tabla:** OPRI
- **Descripción:** Browser Access Printers
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPRI.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Name` | Printer Name | nVarChar | 250 | - |  |  |
| 3 | `UserID` | User ID | Int | 6 | - |  |  |
| 4 | `Desc` | Description | nVarChar | 254 | - |  |  |
| 5 | `Server` | Server | nVarChar | 254 | - |  |  |
| 6 | `Selected` | Select Printer | VarChar | 1 | - | N |  |
| 7 | `DPrinter` | Default Printer | VarChar | 1 | - | N |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
