# EMMSG - EMMSG

- **Tabla:** EMMSG
- **Descripción:** EMMSG
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EMMSG.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ID` | Message ID | nVarChar | 60 | - |  |  |
| 2 | `Service` | Service | nVarChar | 160 | - |  |  |
| 3 | `Operation` | Operation | nVarChar | 60 | - |  |  |
| 4 | `Sender` | Sender ID | nVarChar | 50 | - |  |  |
| 5 | `Receiver` | Receiver ID | nVarChar | 50 | - |  |  |
| 6 | `InOut` | Incoming outgoing indicator | nVarChar | 10 | - |  |  |
| 7 | `BOType` | Business object type | nVarChar | 100 | - |  |  |
| 8 | `BOID` | Business object ID | nVarChar | 30 | - |  |  |
| 9 | `SboBoType` | Business one object type | nVarChar | 100 | - |  |  |
| 10 | `SboBoID` | Business one object ID | nVarChar | 30 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
