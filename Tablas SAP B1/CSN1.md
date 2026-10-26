# CSN1 - Certificate Series - Series

- **Tabla:** CSN1
- **Descripción:** Certificate Series - Series
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CSN1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | [OCSN](OCSN.md) |  |  |
| 2 | `Series` | Series | Int | 6 | - |  |  |
| 3 | `BeginStr` | Prefix | nVarChar | 20 | - |  |  |
| 4 | `InitialNum` | First No. | Int | 11 | - | 1 |  |
| 5 | `NextNum` | Next No. | Int | 11 | - | 1 |  |
| 6 | `LastNum` | Last No. | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId, Series |
