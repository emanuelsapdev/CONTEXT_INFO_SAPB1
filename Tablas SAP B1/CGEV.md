# CGEV - Event Log

- **Tabla:** CGEV
- **Descripción:** Event Log
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CGEV.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `EventID` | Event ID | Identity | 11 | - |  |  |
| 2 | `EventDate` | Date of Event | Date | 8 | - |  |  |
| 3 | `EventTime` | Timestamp of Event | Int | 11 | - |  |  |
| 4 | `UserCode` | Current User ID | nVarChar | 25 | - |  |  |
| 5 | `SourceIP` | Network Address of SAP Business One Client | nVarChar | 64 | - |  |  |
| 6 | `EventType` | Event Type | nVarChar | 32 | - |  |  |
| 7 | `EventDetls` | Event Description | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | EventID |
