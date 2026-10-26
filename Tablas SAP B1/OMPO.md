# OMPO - Value Mapping Object

- **Tabla:** OMPO
- **Descripción:** Value Mapping Object
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OMPO.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ObjectId` | Object ID | Int | 11 | - |  |  |
| 3 | `ObAbsEntry` | Object Internal Number | nVarChar | 100 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| B1_VALUE | Yes | ObjectId, ObAbsEntry |
