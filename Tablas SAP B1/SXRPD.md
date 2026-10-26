# SXRPD - XLR Property Definitions

- **Tabla:** SXRPD
- **Descripción:** XLR Property Definitions
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SXRPD.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `propdefid` | propdefid | Int | 11 | - |  |  |
| 2 | `classid` | classid | Int | 11 | - |  |  |
| 3 | `seqno` | seqno | Int | 11 | - | 0 |  |
| 4 | `name` | name | nVarChar | 50 | - |  |  |
| 5 | `category` | category | nVarChar | 50 | - | 'General' |  |
| 6 | `descriptio` | description | nVarChar | 254 | - |  |  |
| 7 | `type` | type | Int | 11 | - | 0 |  |
| 8 | `minoccurs` | minoccurs | Int | 11 | - | 0 |  |
| 9 | `maxoccurs` | maxoccurs | Int | 11 | - | 999999 |  |
| 10 | `classrefid` | classrefid | Int | 11 | - | 0 |  |
| 11 | `enumid` | enumid | Int | 11 | - | 0 | `0` |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | propdefid |
