# ACEST - CEST Codes

- **Tabla:** ACEST
- **Descripción:** CEST Codes
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACEST.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `CEST` | CEST Code | nVarChar | 32 | - |  |  |
| 3 | `Descr` | Description | Text | 16 | - |  |  |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId, LogInstanc |
| CEST_CODE | Yes | CEST, LogInstanc |
