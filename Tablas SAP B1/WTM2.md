# WTM2 - Confirmation Templates - Stages

- **Tabla:** WTM2
- **Descripción:** Confirmation Templates - Stages
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WTM2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WtmCode` | Code | Int | 11 | [OWTM](OWTM.md) |  |  |
| 2 | `WstCode` | Stage | Int | 11 | [OWST](OWST.md) |  |  |
| 3 | `SortId` | Sort Code | Int | 6 | - | 1 |  |
| 4 | `Remarks` | Description | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WtmCode, WstCode |
