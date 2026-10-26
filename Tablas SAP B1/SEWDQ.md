# SEWDQ - SEWDQ

- **Tabla:** SEWDQ
- **Descripción:** SEWDQ
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SEWDQ.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Absolute Entry | Int | 11 | - |  |  |
| 2 | `CompDbNam` | Company Db Name | nVarChar | 200 | - |  |  |
| 3 | `QueryStr` | The query processed string | Text | 16 | - |  |  |
| 4 | `NumCol` | Number of column in answer | Int | 11 | - |  |  |
| 5 | `NumRow` | Number of rows in answer | Int | 11 | - |  |  |
| 6 | `ResStr` | The format restult string | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, CompDbNam |
