# ORST - Route Stages

- **Tabla:** ORST
- **Descripción:** Route Stages
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORST.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Code | nVarChar | 50 | - |  |  |
| 3 | `Desc` | Description | nVarChar | 100 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 5 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 6 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 7 | `CreateTime` | Generation Time | Int | 6 | - |  |  |
| 8 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SECONDARY | Yes | Code |
