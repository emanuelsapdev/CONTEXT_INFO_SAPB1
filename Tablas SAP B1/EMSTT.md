# EMSTT - EMSTT

- **Tabla:** EMSTT
- **Descripción:** EMSTT
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EMSTT.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MessageID` | Message ID | nVarChar | 60 | - |  |  |
| 2 | `Timestamp` | Timestamp | Date | 8 | - |  |  |
| 3 | `Status` | Status | nVarChar | 30 | - |  |  |
| 4 | `ErrorID` | Error ID | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MessageID, Timestamp, Status |
