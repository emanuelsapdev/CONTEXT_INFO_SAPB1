# SXRRE - XLR Relations

- **Tabla:** SXRRE
- **Descripción:** XLR Relations
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SXRRE.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `relid` | relid | Identity | 11 | - |  |  |
| 2 | `objidfrom` | objidfrom | Int | 11 | - | 0 |  |
| 3 | `propdefid` | propdefid | Int | 11 | - | 0 |  |
| 4 | `seqno` | seqno | Int | 11 | - | 0 |  |
| 5 | `objidto` | objidto | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | relid |
| second | Yes | objidfrom, propdefid, seqno |
