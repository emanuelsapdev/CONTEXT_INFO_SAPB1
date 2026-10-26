# EMIDS - EMIDS

- **Tabla:** EMIDS
- **Descripción:** EMIDS
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EMIDS.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SequenceID` | Event Sequence ID | nVarChar | 60 | - |  |  |
| 2 | `ProcessID` | Processed message ID | nVarChar | 60 | - |  |  |
| 3 | `DispatchID` | Dispached message ID | nVarChar | 60 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SequenceID, DispatchID |
