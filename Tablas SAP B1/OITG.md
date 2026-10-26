# OITG - Item Properties

- **Tabla:** OITG
- **Descripción:** Item Properties
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OITG.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItmsTypCod` | Number | Int | 6 | - |  |  |
| 2 | `ItmsGrpNam` | Property Name | nVarChar | 50 | - |  |  |
| 3 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItmsTypCod |
| GROUP_NAME | Yes | ItmsGrpNam |
