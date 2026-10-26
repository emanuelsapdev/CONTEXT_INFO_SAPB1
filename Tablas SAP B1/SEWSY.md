# SEWSY - SEWSY

- **Tabla:** SEWSY
- **Descripción:** SEWSY
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SEWSY.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `S_USER` | Absolute Key | nVarChar | 16 | - |  |  |
| 2 | `SmpSendAdd` | Smp Server URL | nVarChar | 254 | - |  |  |
| 3 | `SmpInboAdd` | Smp user Inbox URL | nVarChar | 254 | - |  |  |
| 4 | `CollecData` | Communication and trigger flag | VarChar | 1 | - | N | `Y` = CollectData<br>`N` = DontCollectData |
| 5 | `FindSolAdd` | Find Solution URL | nVarChar | 254 | - |  |  |
| 6 | `FeedOptAdd` | Feedback Option URL | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | S_USER |
