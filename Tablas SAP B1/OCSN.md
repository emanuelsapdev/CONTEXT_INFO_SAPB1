# OCSN - Certificate Series

- **Tabla:** OCSN
- **Descripción:** Certificate Series
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCSN.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Code | nVarChar | 4 | - |  |  |
| 3 | `Section` | Section | Int | 11 | [OSEC](OSEC.md) |  |  |
| 4 | `Location` | Location | Int | 11 | [OLCT](OLCT.md) |  |  |
| 5 | `DfltSeries` | Default Series | Int | 6 | - | 0 |  |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| CODE | Yes | Code |
| SECTION | No | Section |
| LOCATION | No | Location |
