# OXAP - XAPP Master Data

- **Tabla:** OXAP
- **Descripción:** XAPP Master Data
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OXAP.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Key of XAPP | Int | 11 | - |  |  |
| 2 | `Name` | Name of XAPP | nVarChar | 250 | - |  |  |
| 3 | `Default` | Is default | VarChar | 1 | - | N |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| NAME | Yes | Name |
