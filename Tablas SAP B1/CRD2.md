# CRD2 - Bussiness Partners - Payment Methods

- **Tabla:** CRD2
- **Descripción:** Bussiness Partners - Payment Methods
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CRD2.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `PymCode` | Payment Method Code | nVarChar | 15 | [OPYM](OPYM.md) |  |  |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 5 | `ObjType` | Object Type | Int | 6 | [ADP1](ADP1.md) | 2 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode, LineNum |
| CRD_PYM | No | CardCode, PymCode |
