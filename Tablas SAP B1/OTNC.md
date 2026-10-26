# OTNC - Transaction Category

- **Tabla:** OTNC
- **Descripción:** Transaction Category
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTNC.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `TransCat` | Transaction Category | nVarChar | 100 | - |  |  |
| 3 | `Locked` | Locked | VarChar | 1 | - | N |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| TRANS | Yes | TransCat |
