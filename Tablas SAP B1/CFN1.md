# CFN1 - Default Common Functions

- **Tabla:** CFN1
- **Descripción:** Default Common Functions
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CFN1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [OCFN](OCFN.md) |  |  |
| 2 | `ItemIndex` | Common Function Item Index | Int | 11 | - |  |  |
| 3 | `UserMenu` | User Menu Flag | VarChar | 1 | - | N | `Y`<br>`N` |
| 4 | `MenuUID` | Menu UID | nVarChar | 50 | - |  |  |
| 5 | `Name` | Name | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, ItemIndex |
