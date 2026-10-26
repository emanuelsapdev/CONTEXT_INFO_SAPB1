# OPCT - Process Checklist Template

- **Tabla:** OPCT
- **Descripción:** Process Checklist Template
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPCT.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `TmplCode` | Template Primary Key | nVarChar | 15 | - |  |  |
| 3 | `TmplName` | Template Name | nVarChar | 100 | - |  |  |
| 4 | `XMLFile` | XML File Contents | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
| TMPLCODE | Yes | TmplCode |
