# OBOI - Count Widget

- **Tabla:** OBOI
- **Descripción:** Count Widget
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBOI.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Count Widget Code | nVarChar | 15 | - |  |  |
| 3 | `Name` | Name | nVarChar | 100 | - |  |  |
| 4 | `QueryId` | Link Query ID | Int | 11 | [OUQR](OUQR.md) |  |  |
| 5 | `QCategory` | Link Query Category | Int | 11 | [OQCN](OQCN.md) |  |  |
| 6 | `Desc` | Description | nVarChar | 200 | - |  |  |
| 7 | `MenuId` | Menu ID | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE | Yes | Code |
