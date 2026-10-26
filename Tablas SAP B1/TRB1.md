# TRB1 - Tax Report Wizard Selected States

- **Tabla:** TRB1
- **Descripción:** Tax Report Wizard Selected States
- **Cantidad de campos:** 2
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TRB1.html

## Campos (2)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OTRB](OTRB.md) |  |  |
| 2 | `State` | State Code | nVarChar | 3 | [OCST](OCST.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, State |
