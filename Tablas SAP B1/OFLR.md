# OFLR - Object Filter

- **Tabla:** OFLR
- **Descripción:** Object Filter
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFLR.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Key | Int | 11 | - |  |  |
| 2 | `FilterName` | Filter Name | nVarChar | 64 | - |  |  |
| 3 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 4 | `TableName` | Table Name | nVarChar | 5 | - |  |  |
| 5 | `VisOrder` | Visible Order | Int | 6 | - |  |  |
| 6 | `StatCol` | Statistics Column | nVarChar | 10 | - |  |  |
| 7 | `UnitCol` | Unit Column | nVarChar | 10 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
