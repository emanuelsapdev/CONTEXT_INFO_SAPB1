# ORSG - Resource Properties

- **Tabla:** ORSG
- **Descripción:** Resource Properties
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORSG.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ResTypCod` | Number | Int | 6 | - |  |  |
| 2 | `ResGrpNam` | Property Name | nVarChar | 50 | - |  |  |
| 3 | `UserSign` | User Signature | nVarChar | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ResTypCod |
| GROUP_NAME | Yes | ResGrpNam |
