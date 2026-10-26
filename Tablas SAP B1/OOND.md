# OOND - Industries

- **Tabla:** OOND
- **Descripción:** Industries
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OOND.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IndCode` | Industry Code | Int | 11 | - |  |  |
| 2 | `IndName` | Industry Name | nVarChar | 40 | - |  |  |
| 3 | `IndDesc` | Industry Description | nVarChar | 120 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IndCode |
| IND_NAME | Yes | IndName |
