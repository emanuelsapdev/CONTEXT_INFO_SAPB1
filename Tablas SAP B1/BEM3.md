# BEM3 - SAP Sustainability Footprint Management Replicated Master Data

- **Tabla:** BEM3
- **Descripción:** SAP Sustainability Footprint Management Replicated Master Data
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BEM3.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Type` | Master Data Type | nVarChar | 20 | - |  |  |
| 2 | `Identifier` | Master Data Identifier | nVarChar | 60 | - |  |  |
| 3 | `RepDate` | Last Replication Date | Date | 8 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Type, Identifier |
| TYPE | No | Type |
| IDENTIFIER | No | Identifier |
