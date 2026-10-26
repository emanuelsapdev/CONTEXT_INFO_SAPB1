# EML1 - E-mail Log - Rows

- **Tabla:** EML1
- **Descripción:** E-mail Log - Rows
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EML1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Absolute entry | Int | 11 | - |  |  |
| 2 | `Line` | Row Number | Int | 11 | - |  |  |
| 3 | `ObjectID` | Document Object ID | Int | 11 | - |  |  |
| 4 | `DocDate` | Posting Date | Date | 8 | - |  |  |
| 5 | `DocEntry` | Doc Internal Number | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, Line |
