# OSEL - Selection Lists

- **Tabla:** OSEL
- **Descripción:** Selection Lists
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSEL.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UserID` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 2 | `FilterName` | Filter Name | nVarChar | 30 | - | _ |  |
| 3 | `FormNum` | Form Number | nVarChar | 20 | - |  |  |
| 4 | `AbsEntry` | Internal ID | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
