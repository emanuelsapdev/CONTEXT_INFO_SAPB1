# OOSR - Information Source

- **Tabla:** OOSR
- **Descripción:** Information Source
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OOSR.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Num` | Sequence No. | Int | 11 | - |  |  |
| 2 | `Descript` | Description | nVarChar | 30 | - |  |  |
| 3 | `SortOrder` | Sort | Int | 6 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Num |
