# CUMF - Folder

- **Tabla:** CUMF
- **Descripción:** Folder
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CUMF.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FolderId` | Folder Key | Int | 11 | - | 0 |  |
| 2 | `FolderName` | Folder Name | nVarChar | 50 | - |  |  |
| 3 | `SortNum` | Sort Number | Int | 11 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `FatherId` | Parent Key | Int | 11 | - | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | FolderId, UserSign |
