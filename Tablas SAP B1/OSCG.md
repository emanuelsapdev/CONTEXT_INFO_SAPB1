# OSCG - Service Category

- **Tabla:** OSCG
- **Descripción:** Service Category
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSCG.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | ID | Int | 11 | - |  |  |
| 2 | `ServiceCtg` | Service Category | nVarChar | 60 | - |  |  |
| 3 | `Descrip` | Description | nVarChar | 120 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE | Yes | ServiceCtg |
