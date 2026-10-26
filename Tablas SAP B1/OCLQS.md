# OCLQS - Question Orders for "Ask AI" App in Web Client

- **Tabla:** OCLQS
- **Descripción:** Question Orders for "Ask AI" App in Web Client
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCLQS.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SeqId` | Internal Question Order ID | Int | 11 | - |  |  |
| 2 | `ObjType` | Source Object | nVarChar | 32 | - |  |  |
| 3 | `UserId` | User ID | Int | 11 | - |  |  |
| 4 | `ViewType` | Type of Linked Object | nVarChar | 20 | - | DetailedViewHeader | `ListView` = List View<br>`DetailedViewHeader` = Detailed View Header<br>`DetailedViewRows` = Detailed View Rows |
| 5 | `DataVers` | Data Version | Int | 11 | - | 1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SeqId |
