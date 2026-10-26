# NNM2 - Series Default

- **Tabla:** NNM2
- **Descripción:** Series Default
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/NNM2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectCode` | Document | nVarChar | 20 | - |  |  |
| 2 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 3 | `Series` | Series | Int | 11 | - |  |  |
| 4 | `DocSubType` | Document Sub-Type | nVarChar | 2 | - | -- |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectCode, DocSubType, UserSign |
| USER | No | UserSign |
