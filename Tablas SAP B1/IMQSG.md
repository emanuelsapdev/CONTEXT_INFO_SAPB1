# IMQSG - Question Suggestions

- **Tabla:** IMQSG
- **Descripción:** Question Suggestions
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IMQSG.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | Internal Number | Identity | 11 | - |  |  |
| 2 | `Content` | Suggestion Content | nVarChar | 254 | - |  |  |
| 3 | `Weight` | Suggestion Weight | Int | 11 | - |  |  |
| 4 | `Time` | Time | Date | 8 | - |  |  |
| 5 | `Owner` | Owner of Suggestion | nVarChar | 25 | - |  |  |
| 6 | `Language` | Language of Suggestion | Int | 11 | - | 3 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
