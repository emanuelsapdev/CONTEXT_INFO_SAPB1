# OSUS - Support Usage Statistics

- **Tabla:** OSUS
- **Descripción:** Support Usage Statistics
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSUS.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Identity | 11 | - |  |  |
| 2 | `SessionID` | Session ID | Int | 11 | - |  |  |
| 3 | `Type` | Type | Int | 11 | - |  |  |
| 4 | `ID` | ID | nVarChar | 254 | - |  |  |
| 5 | `Param` | Param. | nVarChar | 254 | - |  |  |
| 6 | `TimeStamp` | Time Stamp | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
