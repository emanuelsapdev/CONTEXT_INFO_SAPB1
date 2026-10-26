# TRB2 - Tax Report Wizard Selected Tax Types

- **Tabla:** TRB2
- **Descripción:** Tax Report Wizard Selected Tax Types
- **Cantidad de campos:** 2
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TRB2.html

## Campos (2)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OTRB](OTRB.md) |  |  |
| 2 | `StaType` | Tax Authority Type | Int | 11 | [OSTT](OSTT.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, StaType |
