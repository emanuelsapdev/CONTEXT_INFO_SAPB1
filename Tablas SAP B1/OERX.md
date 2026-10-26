# OERX - Excise Register Numbering Ext

- **Tabla:** OERX
- **Descripción:** Excise Register Numbering Ext
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OERX.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ErnId` | Excise Register Numbering ID | Int | 11 | - |  |  |
| 2 | `Location` | Loc. | Int | 11 | [OLCT](OLCT.md) |  |  |
| 3 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ErnId |
| LOC_KEY | Yes | Location |
