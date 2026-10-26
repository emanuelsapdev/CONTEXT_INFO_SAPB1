# OCUL - Customer Usage Statistics Log

- **Tabla:** OCUL
- **Descripción:** Customer Usage Statistics Log
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCUL.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Identity | 11 | - |  |  |
| 2 | `StartRef` | Session Start Reference | Int | 11 | - |  |  |
| 3 | `EventType` | Event Type | Int | 11 | - |  |  |
| 4 | `DateTime` | Date Time | nVarChar | 20 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
