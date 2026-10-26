# SCPT - SCPT

- **Tabla:** SCPT
- **Descripción:** SCPT
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SCPT.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `guid` | Guid | nVarChar | 36 | - |  |  |
| 2 | `fatherId` | Father Id | nVarChar | 36 | - |  |  |
| 3 | `scriptName` | Script Name | nVarChar | 50 | - |  |  |
| 4 | `script` | Script Details | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | guid |
| NAME | Yes | scriptName |
